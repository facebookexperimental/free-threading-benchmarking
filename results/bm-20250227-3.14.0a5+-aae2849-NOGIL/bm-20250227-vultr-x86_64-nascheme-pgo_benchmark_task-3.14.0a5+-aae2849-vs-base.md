# Results vs. base

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: aae2849
- commit date: 2025-02-27
- overall geometric mean: 1.023x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 318 ms: 1.04x slower                                                   |
| docutils       | 2.80 sec                                                               | 2.88 sec: 1.03x slower                                                 |
| html5lib       | 70.9 ms                                                                | 71.8 ms: 1.01x slower                                                  |
| sphinx         | 1.09 sec                                                               | 1.13 sec: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                 | 24.1 ms                                                                | 24.0 ms: 1.00x faster                                                  |
| async_tree_memoization     | 340 ms                                                                 | 346 ms: 1.02x slower                                                   |
| async_tree_none            | 275 ms                                                                 | 280 ms: 1.02x slower                                                   |
| async_tree_memoization_tg  | 307 ms                                                                 | 313 ms: 1.02x slower                                                   |
| async_tree_none_tg         | 237 ms                                                                 | 242 ms: 1.02x slower                                                   |
| async_generators           | 368 ms                                                                 | 377 ms: 1.03x slower                                                   |
| async_tree_io              | 580 ms                                                                 | 602 ms: 1.04x slower                                                   |
| async_tree_io_tg           | 547 ms                                                                 | 576 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 600 ms: 1.15x slower                                                   |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 566 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 212 ms                                                                 | 201 ms: 1.06x faster                                                   |
| float          | 76.5 ms                                                                | 76.2 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.77 ms                                                                | 2.57 ms: 1.08x faster                                                  |
| regex_dna      | 169 ms                                                                 | 163 ms: 1.03x faster                                                   |
| regex_compile  | 156 ms                                                                 | 161 ms: 1.03x slower                                                   |
| regex_v8       | 23.1 ms                                                                | 25.6 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.0 ms                                                                | 12.0 ms: 1.08x faster                                                  |
| tomli_loads          | 2.43 sec                                                               | 2.50 sec: 1.03x slower                                                 |
| json_loads           | 29.4 us                                                                | 30.5 us: 1.04x slower                                                  |
| xml_etree_process    | 70.1 ms                                                                | 75.1 ms: 1.07x slower                                                  |
| xml_etree_generate   | 96.4 ms                                                                | 103 ms: 1.07x slower                                                   |
| unpickle_pure_python | 255 us                                                                 | 278 us: 1.09x slower                                                   |
| pickle_pure_python   | 371 us                                                                 | 408 us: 1.10x slower                                                   |
| xml_etree_iterparse  | 87.2 ms                                                                | 95.8 ms: 1.10x slower                                                  |
| xml_etree_parse      | 128 ms                                                                 | 148 ms: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.68 ms                                                                | 9.79 ms: 1.01x slower                                                  |
| python_startup         | 15.6 ms                                                                | 15.9 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                                  |
| django_template | 43.5 ms                                                                | 44.0 ms: 1.01x slower                                                  |
| genshi_text     | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                  |
| genshi_xml      | 60.0 ms                                                                | 62.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.77 sec                                                               | 2.42 sec: 1.14x faster                                                 |
| telco                      | 8.61 ms                                                                | 7.63 ms: 1.13x faster                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.57 ms: 1.08x faster                                                  |
| json_dumps                 | 13.0 ms                                                                | 12.0 ms: 1.08x faster                                                  |
| meteor_contest             | 128 ms                                                                 | 119 ms: 1.08x faster                                                   |
| fannkuch                   | 496 ms                                                                 | 466 ms: 1.06x faster                                                   |
| pidigits                   | 212 ms                                                                 | 201 ms: 1.06x faster                                                   |
| spectral_norm              | 115 ms                                                                 | 110 ms: 1.05x faster                                                   |
| regex_dna                  | 169 ms                                                                 | 163 ms: 1.03x faster                                                   |
| scimark_fft                | 399 ms                                                                 | 389 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 4.79 sec                                                               | 4.69 sec: 1.02x faster                                                 |
| create_gc_cycles           | 1.30 ms                                                                | 1.27 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.55 ms: 1.01x faster                                                  |
| gc_traversal               | 1.71 ms                                                                | 1.69 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 845 ms                                                                 | 839 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 84.7 ms                                                                | 84.1 ms: 1.01x faster                                                  |
| chaos                      | 70.6 ms                                                                | 70.1 ms: 1.01x faster                                                  |
| nqueens                    | 98.5 ms                                                                | 97.9 ms: 1.01x faster                                                  |
| scimark_sor                | 138 ms                                                                 | 137 ms: 1.00x faster                                                   |
| pprint_pformat             | 1.74 sec                                                               | 1.73 sec: 1.00x faster                                                 |
| coroutines                 | 24.1 ms                                                                | 24.0 ms: 1.00x faster                                                  |
| float                      | 76.5 ms                                                                | 76.2 ms: 1.00x faster                                                  |
| deepcopy_memo              | 38.6 us                                                                | 38.6 us: 1.00x faster                                                  |
| hexiom                     | 7.63 ms                                                                | 7.68 ms: 1.01x slower                                                  |
| mako                       | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                                  |
| go                         | 144 ms                                                                 | 145 ms: 1.01x slower                                                   |
| logging_silent             | 116 ns                                                                 | 117 ns: 1.01x slower                                                   |
| scimark_lu                 | 139 ms                                                                 | 141 ms: 1.01x slower                                                   |
| django_template            | 43.5 ms                                                                | 44.0 ms: 1.01x slower                                                  |
| python_startup_no_site     | 9.68 ms                                                                | 9.79 ms: 1.01x slower                                                  |
| bench_mp_pool              | 95.4 ms                                                                | 96.6 ms: 1.01x slower                                                  |
| html5lib                   | 70.9 ms                                                                | 71.8 ms: 1.01x slower                                                  |
| python_startup             | 15.6 ms                                                                | 15.9 ms: 1.01x slower                                                  |
| async_tree_memoization     | 340 ms                                                                 | 346 ms: 1.02x slower                                                   |
| async_tree_none            | 275 ms                                                                 | 280 ms: 1.02x slower                                                   |
| connected_components       | 494 ms                                                                 | 504 ms: 1.02x slower                                                   |
| async_tree_memoization_tg  | 307 ms                                                                 | 313 ms: 1.02x slower                                                   |
| shortest_path              | 548 ms                                                                 | 560 ms: 1.02x slower                                                   |
| pathlib                    | 19.9 ms                                                                | 20.3 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.04 us                                                                | 2.09 us: 1.02x slower                                                  |
| sqlalchemy_imperative      | 24.0 ms                                                                | 24.5 ms: 1.02x slower                                                  |
| deepcopy                   | 314 us                                                                 | 321 us: 1.02x slower                                                   |
| async_tree_none_tg         | 237 ms                                                                 | 242 ms: 1.02x slower                                                   |
| async_generators           | 368 ms                                                                 | 377 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 201 us                                                                 | 206 us: 1.03x slower                                                   |
| sqlalchemy_declarative     | 156 ms                                                                 | 161 ms: 1.03x slower                                                   |
| deltablue                  | 3.91 ms                                                                | 4.02 ms: 1.03x slower                                                  |
| tomli_loads                | 2.43 sec                                                               | 2.50 sec: 1.03x slower                                                 |
| docutils                   | 2.80 sec                                                               | 2.88 sec: 1.03x slower                                                 |
| dulwich_log                | 83.1 ms                                                                | 85.7 ms: 1.03x slower                                                  |
| regex_compile              | 156 ms                                                                 | 161 ms: 1.03x slower                                                   |
| genshi_text                | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                  |
| generators                 | 31.9 ms                                                                | 33.0 ms: 1.03x slower                                                  |
| sphinx                     | 1.09 sec                                                               | 1.13 sec: 1.03x slower                                                 |
| crypto_pyaes               | 88.3 ms                                                                | 91.3 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 125 ms: 1.03x slower                                                   |
| json_loads                 | 29.4 us                                                                | 30.5 us: 1.04x slower                                                  |
| sqlglot_transpile          | 1.93 ms                                                                | 2.00 ms: 1.04x slower                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 63.7 ms: 1.04x slower                                                  |
| async_tree_io              | 580 ms                                                                 | 602 ms: 1.04x slower                                                   |
| many_optionals             | 1.17 ms                                                                | 1.21 ms: 1.04x slower                                                  |
| logging_format             | 8.31 us                                                                | 8.64 us: 1.04x slower                                                  |
| genshi_xml                 | 60.0 ms                                                                | 62.5 ms: 1.04x slower                                                  |
| pylint                     | 315 ms                                                                 | 328 ms: 1.04x slower                                                   |
| 2to3                       | 305 ms                                                                 | 318 ms: 1.04x slower                                                   |
| sympy_sum                  | 186 ms                                                                 | 194 ms: 1.04x slower                                                   |
| sympy_integrate            | 24.2 ms                                                                | 25.2 ms: 1.04x slower                                                  |
| sqlglot_parse              | 1.60 ms                                                                | 1.67 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 3.18 us                                                                | 3.34 us: 1.05x slower                                                  |
| sympy_str                  | 335 ms                                                                 | 352 ms: 1.05x slower                                                   |
| async_tree_io_tg           | 547 ms                                                                 | 576 ms: 1.05x slower                                                   |
| logging_simple             | 7.22 us                                                                | 7.60 us: 1.05x slower                                                  |
| pycparser                  | 1.19 sec                                                               | 1.26 sec: 1.05x slower                                                 |
| pyflate                    | 507 ms                                                                 | 535 ms: 1.06x slower                                                   |
| richards_super             | 64.5 ms                                                                | 68.2 ms: 1.06x slower                                                  |
| sympy_expand               | 549 ms                                                                 | 580 ms: 1.06x slower                                                   |
| k_core                     | 2.30 sec                                                               | 2.43 sec: 1.06x slower                                                 |
| json                       | 5.15 ms                                                                | 5.47 ms: 1.06x slower                                                  |
| richards                   | 55.5 ms                                                                | 59.2 ms: 1.07x slower                                                  |
| xml_etree_process          | 70.1 ms                                                                | 75.1 ms: 1.07x slower                                                  |
| xml_etree_generate         | 96.4 ms                                                                | 103 ms: 1.07x slower                                                   |
| coverage                   | 96.9 ms                                                                | 104 ms: 1.08x slower                                                   |
| subparsers                 | 25.1 ms                                                                | 27.3 ms: 1.09x slower                                                  |
| unpickle_pure_python       | 255 us                                                                 | 278 us: 1.09x slower                                                   |
| bench_thread_pool          | 3.32 ms                                                                | 3.63 ms: 1.09x slower                                                  |
| pickle_pure_python         | 371 us                                                                 | 408 us: 1.10x slower                                                   |
| xml_etree_iterparse        | 87.2 ms                                                                | 95.8 ms: 1.10x slower                                                  |
| regex_v8                   | 23.1 ms                                                                | 25.6 ms: 1.11x slower                                                  |
| thrift                     | 867 us                                                                 | 980 us: 1.13x slower                                                   |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 600 ms: 1.15x slower                                                   |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 566 ms: 1.15x slower                                                   |
| xml_etree_parse            | 128 ms                                                                 | 148 ms: 1.16x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (4): comprehensions, asyncio_websockets, nbody, raytrace

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.99x