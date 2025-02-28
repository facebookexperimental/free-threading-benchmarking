# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: 8dd8862
- commit date: 2025-02-28
- overall geometric mean: 1.124x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 312 ms: 1.24x slower                                                   |
| docutils       | 2.54 sec                                                               | 2.81 sec: 1.11x slower                                                 |
| sphinx         | 973 ms                                                                 | 1.10 sec: 1.13x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 501 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 536 ms: 1.10x faster                                                   |
| async_tree_none_tg         | 252 ms                                                                 | 232 ms: 1.08x faster                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 547 ms: 1.08x faster                                                   |
| async_tree_io              | 599 ms                                                                 | 583 ms: 1.03x faster                                                   |
| async_tree_memoization_tg  | 306 ms                                                                 | 300 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                   |
| async_tree_none            | 256 ms                                                                 | 273 ms: 1.06x slower                                                   |
| async_tree_memoization     | 311 ms                                                                 | 334 ms: 1.07x slower                                                   |
| coroutines                 | 20.8 ms                                                                | 23.2 ms: 1.11x slower                                                  |
| async_generators           | 316 ms                                                                 | 370 ms: 1.17x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 195 ms: 1.27x faster                                                   |
| float          | 70.7 ms                                                                | 73.8 ms: 1.05x slower                                                  |
| nbody          | 84.7 ms                                                                | 138 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 21.7 ms: 1.13x faster                                                  |
| regex_effbot   | 2.68 ms                                                                | 2.44 ms: 1.10x faster                                                  |
| regex_dna      | 170 ms                                                                 | 157 ms: 1.08x faster                                                   |
| regex_compile  | 125 ms                                                                 | 160 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 89.6 ms                                                                | 84.3 ms: 1.06x faster                                                  |
| xml_etree_parse      | 128 ms                                                                 | 123 ms: 1.05x faster                                                   |
| json_loads           | 28.3 us                                                                | 29.2 us: 1.03x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 11.9 ms: 1.07x slower                                                  |
| xml_etree_generate   | 82.0 ms                                                                | 92.4 ms: 1.13x slower                                                  |
| xml_etree_process    | 57.1 ms                                                                | 66.5 ms: 1.16x slower                                                  |
| pickle_pure_python   | 303 us                                                                 | 367 us: 1.21x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 264 us: 1.27x slower                                                   |
| tomli_loads          | 1.82 sec                                                               | 2.50 sec: 1.37x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.9 ms: 1.07x slower                                                  |
| python_startup_no_site | 7.54 ms                                                                | 9.80 ms: 1.30x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.18x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 61.3 ms: 1.28x slower                                                  |
| django_template | 33.5 ms                                                                | 44.0 ms: 1.31x slower                                                  |
| mako            | 11.5 ms                                                                | 15.7 ms: 1.37x slower                                                  |
| genshi_text     | 20.6 ms                                                                | 28.5 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.34x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 1.71 ms: 2.50x faster                                                  |
| sqlglot_normalize          | 278 ms                                                                 | 124 ms: 2.25x faster                                                   |
| create_gc_cycles           | 1.83 ms                                                                | 1.28 ms: 1.42x faster                                                  |
| pidigits                   | 247 ms                                                                 | 195 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 501 ms: 1.15x faster                                                   |
| regex_v8                   | 24.5 ms                                                                | 21.7 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 536 ms: 1.10x faster                                                   |
| regex_effbot               | 2.68 ms                                                                | 2.44 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.18 us                                                                | 2.00 us: 1.09x faster                                                  |
| async_tree_none_tg         | 252 ms                                                                 | 232 ms: 1.08x faster                                                   |
| regex_dna                  | 170 ms                                                                 | 157 ms: 1.08x faster                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 547 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 89.6 ms                                                                | 84.3 ms: 1.06x faster                                                  |
| xml_etree_parse            | 128 ms                                                                 | 123 ms: 1.05x faster                                                   |
| async_tree_io              | 599 ms                                                                 | 583 ms: 1.03x faster                                                   |
| async_tree_memoization_tg  | 306 ms                                                                 | 300 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                   |
| json_loads                 | 28.3 us                                                                | 29.2 us: 1.03x slower                                                  |
| float                      | 70.7 ms                                                                | 73.8 ms: 1.05x slower                                                  |
| json                       | 4.96 ms                                                                | 5.19 ms: 1.05x slower                                                  |
| pathlib                    | 18.7 ms                                                                | 19.8 ms: 1.06x slower                                                  |
| telco                      | 7.17 ms                                                                | 7.57 ms: 1.06x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.43 sec: 1.06x slower                                                 |
| async_tree_none            | 256 ms                                                                 | 273 ms: 1.06x slower                                                   |
| logging_silent             | 103 ns                                                                 | 109 ns: 1.06x slower                                                   |
| python_startup             | 14.8 ms                                                                | 15.9 ms: 1.07x slower                                                  |
| json_dumps                 | 11.1 ms                                                                | 11.9 ms: 1.07x slower                                                  |
| async_tree_memoization     | 311 ms                                                                 | 334 ms: 1.07x slower                                                   |
| bench_mp_pool              | 88.5 ms                                                                | 96.4 ms: 1.09x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.81 sec: 1.11x slower                                                 |
| coroutines                 | 20.8 ms                                                                | 23.2 ms: 1.11x slower                                                  |
| dulwich_log                | 75.8 ms                                                                | 84.7 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.12 sec                                                               | 4.63 sec: 1.12x slower                                                 |
| xml_etree_generate         | 82.0 ms                                                                | 92.4 ms: 1.13x slower                                                  |
| sphinx                     | 973 ms                                                                 | 1.10 sec: 1.13x slower                                                 |
| pycparser                  | 1.10 sec                                                               | 1.26 sec: 1.14x slower                                                 |
| k_core                     | 2.03 sec                                                               | 2.35 sec: 1.16x slower                                                 |
| xml_etree_process          | 57.1 ms                                                                | 66.5 ms: 1.16x slower                                                  |
| subparsers                 | 21.9 ms                                                                | 25.6 ms: 1.17x slower                                                  |
| pylint                     | 275 ms                                                                 | 321 ms: 1.17x slower                                                   |
| async_generators           | 316 ms                                                                 | 370 ms: 1.17x slower                                                   |
| many_optionals             | 1.01 ms                                                                | 1.19 ms: 1.18x slower                                                  |
| meteor_contest             | 97.8 ms                                                                | 117 ms: 1.20x slower                                                   |
| pickle_pure_python         | 303 us                                                                 | 367 us: 1.21x slower                                                   |
| deepcopy_reduce            | 2.60 us                                                                | 3.15 us: 1.21x slower                                                  |
| deepcopy                   | 252 us                                                                 | 309 us: 1.23x slower                                                   |
| sympy_expand               | 453 ms                                                                 | 559 ms: 1.23x slower                                                   |
| fannkuch                   | 367 ms                                                                 | 453 ms: 1.23x slower                                                   |
| sqlglot_optimize           | 50.5 ms                                                                | 62.3 ms: 1.23x slower                                                  |
| 2to3                       | 251 ms                                                                 | 312 ms: 1.24x slower                                                   |
| sqlalchemy_imperative      | 19.3 ms                                                                | 24.1 ms: 1.25x slower                                                  |
| logging_simple             | 5.90 us                                                                | 7.38 us: 1.25x slower                                                  |
| logging_format             | 6.68 us                                                                | 8.37 us: 1.25x slower                                                  |
| comprehensions             | 15.9 us                                                                | 19.9 us: 1.25x slower                                                  |
| generators                 | 26.3 ms                                                                | 33.0 ms: 1.25x slower                                                  |
| pprint_safe_repr           | 679 ms                                                                 | 856 ms: 1.26x slower                                                   |
| sqlalchemy_declarative     | 126 ms                                                                 | 159 ms: 1.26x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 264 us: 1.27x slower                                                   |
| sympy_integrate            | 19.4 ms                                                                | 24.5 ms: 1.27x slower                                                  |
| spectral_norm              | 88.1 ms                                                                | 112 ms: 1.27x slower                                                   |
| sympy_sum                  | 151 ms                                                                 | 192 ms: 1.27x slower                                                   |
| thrift                     | 718 us                                                                 | 914 us: 1.27x slower                                                   |
| raytrace                   | 254 ms                                                                 | 323 ms: 1.27x slower                                                   |
| sympy_str                  | 269 ms                                                                 | 343 ms: 1.28x slower                                                   |
| scimark_sor                | 109 ms                                                                 | 139 ms: 1.28x slower                                                   |
| sqlglot_transpile          | 1.53 ms                                                                | 1.95 ms: 1.28x slower                                                  |
| pprint_pformat             | 1.38 sec                                                               | 1.76 sec: 1.28x slower                                                 |
| coverage                   | 79.3 ms                                                                | 101 ms: 1.28x slower                                                   |
| regex_compile              | 125 ms                                                                 | 160 ms: 1.28x slower                                                   |
| scimark_lu                 | 109 ms                                                                 | 140 ms: 1.28x slower                                                   |
| typing_runtime_protocols   | 154 us                                                                 | 198 us: 1.28x slower                                                   |
| genshi_xml                 | 47.8 ms                                                                | 61.3 ms: 1.28x slower                                                  |
| deltablue                  | 3.03 ms                                                                | 3.90 ms: 1.28x slower                                                  |
| connected_components       | 387 ms                                                                 | 499 ms: 1.29x slower                                                   |
| shortest_path              | 426 ms                                                                 | 550 ms: 1.29x slower                                                   |
| scimark_fft                | 303 ms                                                                 | 392 ms: 1.29x slower                                                   |
| richards                   | 42.0 ms                                                                | 54.3 ms: 1.29x slower                                                  |
| chaos                      | 53.7 ms                                                                | 69.6 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.54 ms                                                                | 9.80 ms: 1.30x slower                                                  |
| pyflate                    | 393 ms                                                                 | 516 ms: 1.31x slower                                                   |
| go                         | 110 ms                                                                 | 144 ms: 1.31x slower                                                   |
| nqueens                    | 74.9 ms                                                                | 98.4 ms: 1.31x slower                                                  |
| django_template            | 33.5 ms                                                                | 44.0 ms: 1.31x slower                                                  |
| sqlglot_parse              | 1.23 ms                                                                | 1.62 ms: 1.32x slower                                                  |
| deepcopy_memo              | 29.1 us                                                                | 38.5 us: 1.32x slower                                                  |
| richards_super             | 47.7 ms                                                                | 63.4 ms: 1.33x slower                                                  |
| scimark_monte_carlo        | 61.6 ms                                                                | 82.4 ms: 1.34x slower                                                  |
| hexiom                     | 5.65 ms                                                                | 7.57 ms: 1.34x slower                                                  |
| crypto_pyaes               | 65.6 ms                                                                | 88.8 ms: 1.35x slower                                                  |
| tomli_loads                | 1.82 sec                                                               | 2.50 sec: 1.37x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.7 ms: 1.37x slower                                                  |
| scimark_sparse_mat_mult    | 4.13 ms                                                                | 5.67 ms: 1.37x slower                                                  |
| genshi_text                | 20.6 ms                                                                | 28.5 ms: 1.38x slower                                                  |
| nbody                      | 84.7 ms                                                                | 138 ms: 1.63x slower                                                   |
| bench_thread_pool          | 1.03 ms                                                                | 3.62 ms: 3.52x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                           |
Ignored benchmarks (1) of results/bm-20250228-3.14.0a5+-8dd8862-NOGIL/bm-20250228-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-8dd8862.json: html5lib

- Geometric mean (including insignificant results): 1.124x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x