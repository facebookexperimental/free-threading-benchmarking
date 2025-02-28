# Results vs. base

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: 8dd8862
- commit date: 2025-02-28
- overall geometric mean: 1.008x faster
- HPT reliability: 74.60%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 312 ms: 1.02x slower                                                   |
| html5lib       | 70.9 ms                                                                | 70.2 ms: 1.01x faster                                                  |
| sphinx         | 1.09 sec                                                               | 1.10 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                 | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 300 ms: 1.02x faster                                                   |
| async_tree_none_tg         | 237 ms                                                                 | 232 ms: 1.02x faster                                                   |
| async_tree_memoization     | 340 ms                                                                 | 334 ms: 1.02x faster                                                   |
| async_tree_none            | 275 ms                                                                 | 273 ms: 1.01x faster                                                   |
| async_generators           | 368 ms                                                                 | 370 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 501 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 536 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): async_tree_io_tg, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 212 ms                                                                 | 195 ms: 1.09x faster                                                   |
| float          | 76.5 ms                                                                | 73.8 ms: 1.04x faster                                                  |
| nbody          | 135 ms                                                                 | 138 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.77 ms                                                                | 2.44 ms: 1.14x faster                                                  |
| regex_dna      | 169 ms                                                                 | 157 ms: 1.08x faster                                                   |
| regex_v8       | 23.1 ms                                                                | 21.7 ms: 1.06x faster                                                  |
| regex_compile  | 156 ms                                                                 | 160 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.0 ms                                                                | 11.9 ms: 1.09x faster                                                  |
| xml_etree_process    | 70.1 ms                                                                | 66.5 ms: 1.06x faster                                                  |
| xml_etree_parse      | 128 ms                                                                 | 123 ms: 1.04x faster                                                   |
| xml_etree_generate   | 96.4 ms                                                                | 92.4 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 87.2 ms                                                                | 84.3 ms: 1.03x faster                                                  |
| pickle_pure_python   | 371 us                                                                 | 367 us: 1.01x faster                                                   |
| tomli_loads          | 2.43 sec                                                               | 2.50 sec: 1.03x slower                                                 |
| unpickle_pure_python | 255 us                                                                 | 264 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.68 ms                                                                | 9.80 ms: 1.01x slower                                                  |
| python_startup         | 15.6 ms                                                                | 15.9 ms: 1.02x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                  |
| django_template | 43.5 ms                                                                | 44.0 ms: 1.01x slower                                                  |
| genshi_xml      | 60.0 ms                                                                | 61.3 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.77 sec                                                               | 2.43 sec: 1.14x faster                                                 |
| telco                      | 8.61 ms                                                                | 7.57 ms: 1.14x faster                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.44 ms: 1.14x faster                                                  |
| meteor_contest             | 128 ms                                                                 | 117 ms: 1.10x faster                                                   |
| fannkuch                   | 496 ms                                                                 | 453 ms: 1.09x faster                                                   |
| json_dumps                 | 13.0 ms                                                                | 11.9 ms: 1.09x faster                                                  |
| pidigits                   | 212 ms                                                                 | 195 ms: 1.09x faster                                                   |
| regex_dna                  | 169 ms                                                                 | 157 ms: 1.08x faster                                                   |
| regex_v8                   | 23.1 ms                                                                | 21.7 ms: 1.06x faster                                                  |
| logging_silent             | 116 ns                                                                 | 109 ns: 1.06x faster                                                   |
| xml_etree_process          | 70.1 ms                                                                | 66.5 ms: 1.06x faster                                                  |
| xml_etree_parse            | 128 ms                                                                 | 123 ms: 1.04x faster                                                   |
| xml_etree_generate         | 96.4 ms                                                                | 92.4 ms: 1.04x faster                                                  |
| coroutines                 | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                                  |
| float                      | 76.5 ms                                                                | 73.8 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 87.2 ms                                                                | 84.3 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.79 sec                                                               | 4.63 sec: 1.03x faster                                                 |
| scimark_monte_carlo        | 84.7 ms                                                                | 82.4 ms: 1.03x faster                                                  |
| spectral_norm              | 115 ms                                                                 | 112 ms: 1.03x faster                                                   |
| async_tree_memoization_tg  | 307 ms                                                                 | 300 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.04 us                                                                | 2.00 us: 1.02x faster                                                  |
| richards                   | 55.5 ms                                                                | 54.3 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 237 ms                                                                 | 232 ms: 1.02x faster                                                   |
| async_tree_memoization     | 340 ms                                                                 | 334 ms: 1.02x faster                                                   |
| comprehensions             | 20.3 us                                                                | 19.9 us: 1.02x faster                                                  |
| scimark_fft                | 399 ms                                                                 | 392 ms: 1.02x faster                                                   |
| richards_super             | 64.5 ms                                                                | 63.4 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 201 us                                                                 | 198 us: 1.02x faster                                                   |
| deepcopy                   | 314 us                                                                 | 309 us: 1.02x faster                                                   |
| chaos                      | 70.6 ms                                                                | 69.6 ms: 1.01x faster                                                  |
| pickle_pure_python         | 371 us                                                                 | 367 us: 1.01x faster                                                   |
| create_gc_cycles           | 1.30 ms                                                                | 1.28 ms: 1.01x faster                                                  |
| html5lib                   | 70.9 ms                                                                | 70.2 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.18 us                                                                | 3.15 us: 1.01x faster                                                  |
| hexiom                     | 7.63 ms                                                                | 7.57 ms: 1.01x faster                                                  |
| async_tree_none            | 275 ms                                                                 | 273 ms: 1.01x faster                                                   |
| mako                       | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                  |
| pathlib                    | 19.9 ms                                                                | 19.8 ms: 1.00x faster                                                  |
| go                         | 144 ms                                                                 | 144 ms: 1.00x faster                                                   |
| deepcopy_memo              | 38.6 us                                                                | 38.5 us: 1.00x faster                                                  |
| raytrace                   | 324 ms                                                                 | 323 ms: 1.00x faster                                                   |
| async_generators           | 368 ms                                                                 | 370 ms: 1.01x slower                                                   |
| crypto_pyaes               | 88.3 ms                                                                | 88.8 ms: 1.01x slower                                                  |
| scimark_sor                | 138 ms                                                                 | 139 ms: 1.01x slower                                                   |
| logging_format             | 8.31 us                                                                | 8.37 us: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.67 ms: 1.01x slower                                                  |
| sphinx                     | 1.09 sec                                                               | 1.10 sec: 1.01x slower                                                 |
| connected_components       | 494 ms                                                                 | 499 ms: 1.01x slower                                                   |
| bench_mp_pool              | 95.4 ms                                                                | 96.4 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.74 sec                                                               | 1.76 sec: 1.01x slower                                                 |
| sqlglot_parse              | 1.60 ms                                                                | 1.62 ms: 1.01x slower                                                  |
| sqlglot_transpile          | 1.93 ms                                                                | 1.95 ms: 1.01x slower                                                  |
| python_startup_no_site     | 9.68 ms                                                                | 9.80 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 845 ms                                                                 | 856 ms: 1.01x slower                                                   |
| django_template            | 43.5 ms                                                                | 44.0 ms: 1.01x slower                                                  |
| sympy_integrate            | 24.2 ms                                                                | 24.5 ms: 1.02x slower                                                  |
| python_startup             | 15.6 ms                                                                | 15.9 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 62.3 ms: 1.02x slower                                                  |
| subparsers                 | 25.1 ms                                                                | 25.6 ms: 1.02x slower                                                  |
| many_optionals             | 1.17 ms                                                                | 1.19 ms: 1.02x slower                                                  |
| pyflate                    | 507 ms                                                                 | 516 ms: 1.02x slower                                                   |
| dulwich_log                | 83.1 ms                                                                | 84.7 ms: 1.02x slower                                                  |
| sympy_expand               | 549 ms                                                                 | 559 ms: 1.02x slower                                                   |
| nbody                      | 135 ms                                                                 | 138 ms: 1.02x slower                                                   |
| sqlalchemy_declarative     | 156 ms                                                                 | 159 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 501 ms: 1.02x slower                                                   |
| sqlglot_normalize          | 121 ms                                                                 | 124 ms: 1.02x slower                                                   |
| genshi_xml                 | 60.0 ms                                                                | 61.3 ms: 1.02x slower                                                  |
| k_core                     | 2.30 sec                                                               | 2.35 sec: 1.02x slower                                                 |
| 2to3                       | 305 ms                                                                 | 312 ms: 1.02x slower                                                   |
| logging_simple             | 7.22 us                                                                | 7.38 us: 1.02x slower                                                  |
| regex_compile              | 156 ms                                                                 | 160 ms: 1.02x slower                                                   |
| sympy_str                  | 335 ms                                                                 | 343 ms: 1.02x slower                                                   |
| tomli_loads                | 2.43 sec                                                               | 2.50 sec: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 536 ms: 1.03x slower                                                   |
| sympy_sum                  | 186 ms                                                                 | 192 ms: 1.03x slower                                                   |
| unpickle_pure_python       | 255 us                                                                 | 264 us: 1.03x slower                                                   |
| generators                 | 31.9 ms                                                                | 33.0 ms: 1.03x slower                                                  |
| coverage                   | 96.9 ms                                                                | 101 ms: 1.05x slower                                                   |
| thrift                     | 867 us                                                                 | 914 us: 1.05x slower                                                   |
| pycparser                  | 1.19 sec                                                               | 1.26 sec: 1.06x slower                                                 |
| bench_thread_pool          | 3.32 ms                                                                | 3.62 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (14): json_loads, deltablue, nqueens, genshi_text, gc_traversal, async_tree_io_tg, asyncio_websockets, scimark_lu, shortest_path, sqlalchemy_imperative, async_tree_io, docutils, json, pylint

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 74.60% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x