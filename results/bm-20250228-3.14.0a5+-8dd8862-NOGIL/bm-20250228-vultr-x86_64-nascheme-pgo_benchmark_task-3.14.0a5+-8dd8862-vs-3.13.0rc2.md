# Results vs. 3.13.0rc2

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: 8dd8862
- commit date: 2025-02-28
- overall geometric mean: 1.071x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 312 ms: 1.20x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                 |
| html5lib       | 68.6 ms                                                                | 70.2 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 547 ms: 1.65x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.43x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.37x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 273 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 536 ms: 1.24x faster                                                   |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                   |
| float          | 76.7 ms                                                                | 73.8 ms: 1.04x faster                                                  |
| nbody          | 85.3 ms                                                                | 138 ms: 1.61x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.44 ms: 1.31x faster                                                  |
| regex_dna      | 189 ms                                                                 | 157 ms: 1.20x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 160 ms: 1.22x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 123 ms: 1.11x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 92.4 ms: 1.08x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.9 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 66.5 ms: 1.12x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.50 sec: 1.24x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 367 us: 1.26x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 264 us: 1.27x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.80 ms: 1.32x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 61.3 ms: 1.25x slower                                                  |
| django_template | 34.2 ms                                                                | 44.0 ms: 1.29x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 28.5 ms: 1.31x slower                                                  |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 547 ms: 1.65x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.43x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.37x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.44 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 273 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 536 ms: 1.24x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 157 ms: 1.20x faster                                                   |
| deepcopy                   | 357 us                                                                 | 309 us: 1.16x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 123 ms: 1.11x faster                                                   |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.28 ms: 1.04x faster                                                  |
| float                      | 76.7 ms                                                                | 73.8 ms: 1.04x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.57 ms: 1.03x faster                                                  |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.15 us: 1.01x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 38.5 us: 1.01x slower                                                  |
| go                         | 141 ms                                                                 | 144 ms: 1.02x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 70.2 ms: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.43 sec: 1.04x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 139 ms: 1.04x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.63 sec: 1.04x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                   |
| json                       | 4.98 ms                                                                | 5.19 ms: 1.04x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 92.4 ms: 1.08x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 109 ns: 1.11x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.9 ms: 1.12x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 66.5 ms: 1.12x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 392 ms: 1.12x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.26 sec: 1.13x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 84.7 ms: 1.14x slower                                                  |
| pyflate                    | 449 ms                                                                 | 516 ms: 1.15x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 117 ms: 1.15x slower                                                   |
| generators                 | 28.5 ms                                                                | 33.0 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 124 ms: 1.17x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 62.3 ms: 1.18x slower                                                  |
| thrift                     | 772 us                                                                 | 914 us: 1.18x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 856 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.67 ms: 1.19x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.38 us: 1.20x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.9 us: 1.20x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 453 ms: 1.20x slower                                                   |
| 2to3                       | 259 ms                                                                 | 312 ms: 1.20x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.37 us: 1.21x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.76 sec: 1.21x slower                                                 |
| regex_compile              | 131 ms                                                                 | 160 ms: 1.22x slower                                                   |
| richards                   | 44.4 ms                                                                | 54.3 ms: 1.22x slower                                                  |
| coverage                   | 82.5 ms                                                                | 101 ms: 1.23x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 559 ms: 1.23x slower                                                   |
| chaos                      | 56.3 ms                                                                | 69.6 ms: 1.24x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.50 sec: 1.24x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 192 ms: 1.25x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 61.3 ms: 1.25x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.4 ms: 1.25x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 343 ms: 1.25x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.95 ms: 1.25x slower                                                  |
| richards_super             | 50.4 ms                                                                | 63.4 ms: 1.26x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 367 us: 1.26x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.90 ms: 1.26x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 98.4 ms: 1.27x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 264 us: 1.27x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.57 ms: 1.27x slower                                                  |
| django_template            | 34.2 ms                                                                | 44.0 ms: 1.29x slower                                                  |
| raytrace                   | 250 ms                                                                 | 323 ms: 1.29x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.62 ms: 1.30x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 88.8 ms: 1.30x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.5 ms: 1.31x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.80 ms: 1.32x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| nbody                      | 85.3 ms                                                                | 138 ms: 1.61x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.62 ms: 3.91x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 96.4 ms: 8.76x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-8dd8862-NOGIL/bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.071x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x