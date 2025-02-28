# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: aae2849
- commit date: 2025-02-27
- overall geometric mean: 1.150x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 318 ms: 1.27x slower                                                   |
| docutils       | 2.54 sec                                                               | 2.88 sec: 1.13x slower                                                 |
| sphinx         | 973 ms                                                                 | 1.13 sec: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 252 ms                                                                 | 242 ms: 1.04x faster                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 576 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 566 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 512 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 600 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 306 ms                                                                 | 313 ms: 1.02x slower                                                   |
| async_tree_none            | 256 ms                                                                 | 280 ms: 1.09x slower                                                   |
| async_tree_memoization     | 311 ms                                                                 | 346 ms: 1.11x slower                                                   |
| coroutines                 | 20.8 ms                                                                | 24.0 ms: 1.15x slower                                                  |
| async_generators           | 316 ms                                                                 | 377 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 201 ms: 1.23x faster                                                   |
| float          | 70.7 ms                                                                | 76.2 ms: 1.08x slower                                                  |
| nbody          | 84.7 ms                                                                | 135 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.68 ms                                                                | 2.57 ms: 1.04x faster                                                  |
| regex_dna      | 170 ms                                                                 | 163 ms: 1.04x faster                                                   |
| regex_v8       | 24.5 ms                                                                | 25.6 ms: 1.04x slower                                                  |
| regex_compile  | 125 ms                                                                 | 161 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 89.6 ms                                                                | 95.8 ms: 1.07x slower                                                  |
| json_loads           | 28.3 us                                                                | 30.5 us: 1.08x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 12.0 ms: 1.09x slower                                                  |
| xml_etree_parse      | 128 ms                                                                 | 148 ms: 1.16x slower                                                   |
| xml_etree_generate   | 82.0 ms                                                                | 103 ms: 1.26x slower                                                   |
| xml_etree_process    | 57.1 ms                                                                | 75.1 ms: 1.31x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 278 us: 1.33x slower                                                   |
| pickle_pure_python   | 303 us                                                                 | 408 us: 1.35x slower                                                   |
| tomli_loads          | 1.82 sec                                                               | 2.50 sec: 1.37x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.9 ms: 1.07x slower                                                  |
| python_startup_no_site | 7.54 ms                                                                | 9.79 ms: 1.30x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.18x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 62.5 ms: 1.31x slower                                                  |
| django_template | 33.5 ms                                                                | 44.0 ms: 1.31x slower                                                  |
| mako            | 11.5 ms                                                                | 15.9 ms: 1.39x slower                                                  |
| genshi_text     | 20.6 ms                                                                | 29.5 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.36x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 1.69 ms: 2.52x faster                                                  |
| sqlglot_normalize          | 278 ms                                                                 | 125 ms: 2.22x faster                                                   |
| create_gc_cycles           | 1.83 ms                                                                | 1.27 ms: 1.44x faster                                                  |
| pidigits                   | 247 ms                                                                 | 201 ms: 1.23x faster                                                   |
| regex_effbot               | 2.68 ms                                                                | 2.57 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.18 us                                                                | 2.09 us: 1.04x faster                                                  |
| regex_dna                  | 170 ms                                                                 | 163 ms: 1.04x faster                                                   |
| async_tree_none_tg         | 252 ms                                                                 | 242 ms: 1.04x faster                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 576 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 566 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 512 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 600 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 306 ms                                                                 | 313 ms: 1.02x slower                                                   |
| regex_v8                   | 24.5 ms                                                                | 25.6 ms: 1.04x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.42 sec: 1.06x slower                                                 |
| telco                      | 7.17 ms                                                                | 7.63 ms: 1.06x slower                                                  |
| xml_etree_iterparse        | 89.6 ms                                                                | 95.8 ms: 1.07x slower                                                  |
| python_startup             | 14.8 ms                                                                | 15.9 ms: 1.07x slower                                                  |
| json_loads                 | 28.3 us                                                                | 30.5 us: 1.08x slower                                                  |
| float                      | 70.7 ms                                                                | 76.2 ms: 1.08x slower                                                  |
| pathlib                    | 18.7 ms                                                                | 20.3 ms: 1.08x slower                                                  |
| json_dumps                 | 11.1 ms                                                                | 12.0 ms: 1.09x slower                                                  |
| async_tree_none            | 256 ms                                                                 | 280 ms: 1.09x slower                                                   |
| bench_mp_pool              | 88.5 ms                                                                | 96.6 ms: 1.09x slower                                                  |
| json                       | 4.96 ms                                                                | 5.47 ms: 1.10x slower                                                  |
| async_tree_memoization     | 311 ms                                                                 | 346 ms: 1.11x slower                                                   |
| dulwich_log                | 75.8 ms                                                                | 85.7 ms: 1.13x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.88 sec: 1.13x slower                                                 |
| bpe_tokeniser              | 4.12 sec                                                               | 4.69 sec: 1.14x slower                                                 |
| pycparser                  | 1.10 sec                                                               | 1.26 sec: 1.14x slower                                                 |
| logging_silent             | 103 ns                                                                 | 117 ns: 1.14x slower                                                   |
| coroutines                 | 20.8 ms                                                                | 24.0 ms: 1.15x slower                                                  |
| xml_etree_parse            | 128 ms                                                                 | 148 ms: 1.16x slower                                                   |
| sphinx                     | 973 ms                                                                 | 1.13 sec: 1.16x slower                                                 |
| pylint                     | 275 ms                                                                 | 328 ms: 1.19x slower                                                   |
| async_generators           | 316 ms                                                                 | 377 ms: 1.19x slower                                                   |
| k_core                     | 2.03 sec                                                               | 2.43 sec: 1.20x slower                                                 |
| many_optionals             | 1.01 ms                                                                | 1.21 ms: 1.21x slower                                                  |
| meteor_contest             | 97.8 ms                                                                | 119 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 679 ms                                                                 | 839 ms: 1.23x slower                                                   |
| spectral_norm              | 88.1 ms                                                                | 110 ms: 1.24x slower                                                   |
| subparsers                 | 21.9 ms                                                                | 27.3 ms: 1.25x slower                                                  |
| generators                 | 26.3 ms                                                                | 33.0 ms: 1.25x slower                                                  |
| pprint_pformat             | 1.38 sec                                                               | 1.73 sec: 1.26x slower                                                 |
| sqlglot_optimize           | 50.5 ms                                                                | 63.7 ms: 1.26x slower                                                  |
| xml_etree_generate         | 82.0 ms                                                                | 103 ms: 1.26x slower                                                   |
| scimark_sor                | 109 ms                                                                 | 137 ms: 1.26x slower                                                   |
| 2to3                       | 251 ms                                                                 | 318 ms: 1.27x slower                                                   |
| fannkuch                   | 367 ms                                                                 | 466 ms: 1.27x slower                                                   |
| sqlalchemy_imperative      | 19.3 ms                                                                | 24.5 ms: 1.27x slower                                                  |
| deepcopy                   | 252 us                                                                 | 321 us: 1.27x slower                                                   |
| sqlalchemy_declarative     | 126 ms                                                                 | 161 ms: 1.27x slower                                                   |
| comprehensions             | 15.9 us                                                                | 20.3 us: 1.27x slower                                                  |
| raytrace                   | 254 ms                                                                 | 325 ms: 1.28x slower                                                   |
| sympy_expand               | 453 ms                                                                 | 580 ms: 1.28x slower                                                   |
| scimark_fft                | 303 ms                                                                 | 389 ms: 1.28x slower                                                   |
| deepcopy_reduce            | 2.60 us                                                                | 3.34 us: 1.28x slower                                                  |
| sympy_sum                  | 151 ms                                                                 | 194 ms: 1.29x slower                                                   |
| logging_simple             | 5.90 us                                                                | 7.60 us: 1.29x slower                                                  |
| regex_compile              | 125 ms                                                                 | 161 ms: 1.29x slower                                                   |
| logging_format             | 6.68 us                                                                | 8.64 us: 1.29x slower                                                  |
| scimark_lu                 | 109 ms                                                                 | 141 ms: 1.29x slower                                                   |
| python_startup_no_site     | 7.54 ms                                                                | 9.79 ms: 1.30x slower                                                  |
| sympy_integrate            | 19.4 ms                                                                | 25.2 ms: 1.30x slower                                                  |
| connected_components       | 387 ms                                                                 | 504 ms: 1.30x slower                                                   |
| chaos                      | 53.7 ms                                                                | 70.1 ms: 1.31x slower                                                  |
| nqueens                    | 74.9 ms                                                                | 97.9 ms: 1.31x slower                                                  |
| sympy_str                  | 269 ms                                                                 | 352 ms: 1.31x slower                                                   |
| genshi_xml                 | 47.8 ms                                                                | 62.5 ms: 1.31x slower                                                  |
| sqlglot_transpile          | 1.53 ms                                                                | 2.00 ms: 1.31x slower                                                  |
| django_template            | 33.5 ms                                                                | 44.0 ms: 1.31x slower                                                  |
| shortest_path              | 426 ms                                                                 | 560 ms: 1.31x slower                                                   |
| xml_etree_process          | 57.1 ms                                                                | 75.1 ms: 1.31x slower                                                  |
| coverage                   | 79.3 ms                                                                | 104 ms: 1.31x slower                                                   |
| deepcopy_memo              | 29.1 us                                                                | 38.6 us: 1.32x slower                                                  |
| deltablue                  | 3.03 ms                                                                | 4.02 ms: 1.32x slower                                                  |
| go                         | 110 ms                                                                 | 145 ms: 1.33x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 278 us: 1.33x slower                                                   |
| typing_runtime_protocols   | 154 us                                                                 | 206 us: 1.34x slower                                                   |
| scimark_sparse_mat_mult    | 4.13 ms                                                                | 5.55 ms: 1.35x slower                                                  |
| pickle_pure_python         | 303 us                                                                 | 408 us: 1.35x slower                                                   |
| sqlglot_parse              | 1.23 ms                                                                | 1.67 ms: 1.36x slower                                                  |
| hexiom                     | 5.65 ms                                                                | 7.68 ms: 1.36x slower                                                  |
| pyflate                    | 393 ms                                                                 | 535 ms: 1.36x slower                                                   |
| thrift                     | 718 us                                                                 | 980 us: 1.36x slower                                                   |
| scimark_monte_carlo        | 61.6 ms                                                                | 84.1 ms: 1.37x slower                                                  |
| tomli_loads                | 1.82 sec                                                               | 2.50 sec: 1.37x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.9 ms: 1.39x slower                                                  |
| crypto_pyaes               | 65.6 ms                                                                | 91.3 ms: 1.39x slower                                                  |
| richards                   | 42.0 ms                                                                | 59.2 ms: 1.41x slower                                                  |
| richards_super             | 47.7 ms                                                                | 68.2 ms: 1.43x slower                                                  |
| genshi_text                | 20.6 ms                                                                | 29.5 ms: 1.43x slower                                                  |
| nbody                      | 84.7 ms                                                                | 135 ms: 1.60x slower                                                   |
| bench_thread_pool          | 1.03 ms                                                                | 3.63 ms: 3.53x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.19x slower                                                           |

Benchmark hidden because not significant (1): async_tree_io
Ignored benchmarks (1) of results/bm-20250227-3.14.0a5+-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849.json: html5lib

- Geometric mean (including insignificant results): 1.150x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.19x