# Results vs. 3.12.6

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: 8dd8862
- commit date: 2025-02-28
- overall geometric mean: 1.039x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 312 ms: 1.19x slower                                                   |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 232 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 536 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.8 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 138 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.44 ms: 1.30x faster                                                  |
| regex_dna      | 168 ms                                                 | 157 ms: 1.07x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| regex_compile  | 142 ms                                                 | 160 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 123 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 92.4 ms: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 66.5 ms: 1.13x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.50 sec: 1.19x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 264 us: 1.20x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.80 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.3 ms: 1.22x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                  |
| django_template | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.03x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 232 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 536 ms: 1.33x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.44 ms: 1.30x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| deepcopy                   | 352 us                                                 | 309 us: 1.14x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 123 ms: 1.13x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.00 us: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 73.8 ms: 1.09x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                  |
| regex_dna                  | 168 ms                                                 | 157 ms: 1.07x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 38.5 us: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.63 sec: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.43 sec: 1.00x slower                                                 |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.15 us: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                   |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                 |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 84.7 ms: 1.07x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.26 sec: 1.08x slower                                                 |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 92.4 ms: 1.08x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.10x slower                                                  |
| chaos                      | 62.8 ms                                                | 69.6 ms: 1.11x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.38 us: 1.11x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 159 ms: 1.12x slower                                                   |
| regex_compile              | 142 ms                                                 | 160 ms: 1.12x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 66.5 ms: 1.13x slower                                                  |
| meteor_contest             | 104 ms                                                 | 117 ms: 1.13x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.90 ms: 1.13x slower                                                  |
| logging_format             | 7.35 us                                                | 8.37 us: 1.14x slower                                                  |
| scimark_fft                | 342 ms                                                 | 392 ms: 1.15x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 856 ms: 1.15x slower                                                   |
| pyflate                    | 448 ms                                                 | 516 ms: 1.15x slower                                                   |
| thrift                     | 791 us                                                 | 914 us: 1.15x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 192 ms: 1.16x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 88.8 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.76 sec: 1.16x slower                                                 |
| telco                      | 6.53 ms                                                | 7.57 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 124 ms: 1.16x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.95 ms: 1.17x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 62.3 ms: 1.17x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.28 ms: 1.17x slower                                                  |
| sympy_str                  | 292 ms                                                 | 343 ms: 1.18x slower                                                   |
| richards                   | 45.9 ms                                                | 54.3 ms: 1.18x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.50 sec: 1.19x slower                                                 |
| 2to3                       | 264 ms                                                 | 312 ms: 1.19x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.5 ms: 1.19x slower                                                  |
| sympy_expand               | 468 ms                                                 | 559 ms: 1.20x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 264 us: 1.20x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.62 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 82.4 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                   |
| fannkuch                   | 372 ms                                                 | 453 ms: 1.22x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 61.3 ms: 1.22x slower                                                  |
| richards_super             | 51.9 ms                                                | 63.4 ms: 1.22x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.57 ms: 1.23x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.4 ms: 1.23x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                  |
| django_template            | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.80 ms: 1.37x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.42x slower                                                   |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 138 ms: 1.54x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.62 ms: 3.84x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 96.4 ms: 8.93x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (2): logging_silent, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-8dd8862-NOGIL/bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.039x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x