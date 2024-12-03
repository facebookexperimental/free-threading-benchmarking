# Results vs. default_base_vs_NOGIL

- fork: dpdani
- ref: gh_117657_tsan_pymem
- machine: linux-x86_64
- commit hash: 6c5cec5
- commit date: 2024-12-03
- overall geometric mean: 1.290x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 376 ms: 1.45x slower                                                   |
| docutils       | 2.58 sec                                                               | 3.20 sec: 1.24x slower                                                 |
| sphinx         | 997 ms                                                                 | 1.23 sec: 1.23x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.30x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                   |
| coroutines                 | 22.5 ms                                                                | 28.1 ms: 1.25x slower                                                  |
| async_generators           | 366 ms                                                                 | 465 ms: 1.27x slower                                                   |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 621 ms: 1.28x slower                                                   |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 653 ms: 1.30x slower                                                   |
| async_tree_io_tg           | 629 ms                                                                 | 861 ms: 1.37x slower                                                   |
| async_tree_none_tg         | 264 ms                                                                 | 364 ms: 1.38x slower                                                   |
| async_tree_io              | 629 ms                                                                 | 886 ms: 1.41x slower                                                   |
| async_tree_none            | 278 ms                                                                 | 397 ms: 1.43x slower                                                   |
| async_tree_memoization     | 341 ms                                                                 | 488 ms: 1.43x slower                                                   |
| async_tree_memoization_tg  | 314 ms                                                                 | 460 ms: 1.47x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.32x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 95.5 ms                                                                | 130 ms: 1.36x slower                                                   |
| float          | 79.2 ms                                                                | 143 ms: 1.80x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.34x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.79 ms                                                                | 2.89 ms: 1.04x slower                                                  |
| regex_dna      | 171 ms                                                                 | 183 ms: 1.07x slower                                                   |
| regex_v8       | 23.7 ms                                                                | 26.0 ms: 1.10x slower                                                  |
| regex_compile  | 131 ms                                                                 | 191 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.3 ms                                                                | 94.4 ms: 1.02x slower                                                  |
| json_loads           | 25.4 us                                                                | 28.0 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.8 ms                                                                | 102 ms: 1.18x slower                                                   |
| json_dumps           | 11.4 ms                                                                | 14.5 ms: 1.27x slower                                                  |
| tomli_loads          | 2.10 sec                                                               | 2.74 sec: 1.30x slower                                                 |
| xml_etree_process    | 60.1 ms                                                                | 81.9 ms: 1.36x slower                                                  |
| unpickle_pure_python | 222 us                                                                 | 379 us: 1.70x slower                                                   |
| pickle_pure_python   | 322 us                                                                 | 556 us: 1.73x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.27x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 17.5 ms: 1.19x slower                                                  |
| python_startup_no_site | 7.50 ms                                                                | 10.3 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 66.0 ms: 1.31x slower                                                  |
| genshi_text     | 22.1 ms                                                                | 33.2 ms: 1.50x slower                                                  |
| django_template | 36.3 ms                                                                | 55.4 ms: 1.53x slower                                                  |
| mako            | 11.6 ms                                                                | 19.6 ms: 1.68x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.50x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 4.28 ms                                                                | 3.53 ms: 1.21x faster                                                  |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                   |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                   |
| xml_etree_iterparse        | 92.3 ms                                                                | 94.4 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.82 ms                                                                | 1.87 ms: 1.02x slower                                                  |
| regex_effbot               | 2.79 ms                                                                | 2.89 ms: 1.04x slower                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.33 us: 1.05x slower                                                  |
| regex_dna                  | 171 ms                                                                 | 183 ms: 1.07x slower                                                   |
| regex_v8                   | 23.7 ms                                                                | 26.0 ms: 1.10x slower                                                  |
| json_loads                 | 25.4 us                                                                | 28.0 us: 1.10x slower                                                  |
| json                       | 4.56 ms                                                                | 5.06 ms: 1.11x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.6 ms: 1.13x slower                                                  |
| spectral_norm              | 113 ms                                                                 | 129 ms: 1.14x slower                                                   |
| k_core                     | 2.08 sec                                                               | 2.43 sec: 1.17x slower                                                 |
| scimark_fft                | 338 ms                                                                 | 398 ms: 1.18x slower                                                   |
| xml_etree_generate         | 85.8 ms                                                                | 102 ms: 1.18x slower                                                   |
| python_startup             | 14.7 ms                                                                | 17.5 ms: 1.19x slower                                                  |
| telco                      | 7.37 ms                                                                | 9.03 ms: 1.23x slower                                                  |
| bench_mp_pool              | 89.6 ms                                                                | 110 ms: 1.23x slower                                                   |
| sphinx                     | 997 ms                                                                 | 1.23 sec: 1.23x slower                                                 |
| docutils                   | 2.58 sec                                                               | 3.20 sec: 1.24x slower                                                 |
| bpe_tokeniser              | 4.34 sec                                                               | 5.40 sec: 1.25x slower                                                 |
| coroutines                 | 22.5 ms                                                                | 28.1 ms: 1.25x slower                                                  |
| shortest_path              | 442 ms                                                                 | 560 ms: 1.27x slower                                                   |
| json_dumps                 | 11.4 ms                                                                | 14.5 ms: 1.27x slower                                                  |
| async_generators           | 366 ms                                                                 | 465 ms: 1.27x slower                                                   |
| coverage                   | 78.9 ms                                                                | 100 ms: 1.27x slower                                                   |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 621 ms: 1.28x slower                                                   |
| connected_components       | 402 ms                                                                 | 513 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 4.47 ms                                                                | 5.73 ms: 1.28x slower                                                  |
| mdp                        | 2.34 sec                                                               | 3.02 sec: 1.29x slower                                                 |
| dulwich_log                | 76.2 ms                                                                | 98.5 ms: 1.29x slower                                                  |
| nqueens                    | 79.8 ms                                                                | 104 ms: 1.30x slower                                                   |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 653 ms: 1.30x slower                                                   |
| tomli_loads                | 2.10 sec                                                               | 2.74 sec: 1.30x slower                                                 |
| genshi_xml                 | 50.5 ms                                                                | 66.0 ms: 1.31x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.36 ms: 1.31x slower                                                  |
| deepcopy                   | 266 us                                                                 | 351 us: 1.32x slower                                                   |
| meteor_contest             | 100 ms                                                                 | 133 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 157 us                                                                 | 208 us: 1.32x slower                                                   |
| fannkuch                   | 378 ms                                                                 | 500 ms: 1.33x slower                                                   |
| generators                 | 29.1 ms                                                                | 38.9 ms: 1.34x slower                                                  |
| nbody                      | 95.5 ms                                                                | 130 ms: 1.36x slower                                                   |
| xml_etree_process          | 60.1 ms                                                                | 81.9 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.50 ms                                                                | 10.3 ms: 1.37x slower                                                  |
| async_tree_io_tg           | 629 ms                                                                 | 861 ms: 1.37x slower                                                   |
| crypto_pyaes               | 67.6 ms                                                                | 92.8 ms: 1.37x slower                                                  |
| sqlglot_optimize           | 54.1 ms                                                                | 74.4 ms: 1.38x slower                                                  |
| async_tree_none_tg         | 264 ms                                                                 | 364 ms: 1.38x slower                                                   |
| pylint                     | 285 ms                                                                 | 394 ms: 1.38x slower                                                   |
| sqlglot_normalize          | 107 ms                                                                 | 149 ms: 1.39x slower                                                   |
| deepcopy_reduce            | 2.68 us                                                                | 3.72 us: 1.39x slower                                                  |
| async_tree_io              | 629 ms                                                                 | 886 ms: 1.41x slower                                                   |
| pycparser                  | 1.13 sec                                                               | 1.60 sec: 1.42x slower                                                 |
| deepcopy_memo              | 31.1 us                                                                | 44.2 us: 1.42x slower                                                  |
| async_tree_none            | 278 ms                                                                 | 397 ms: 1.43x slower                                                   |
| async_tree_memoization     | 341 ms                                                                 | 488 ms: 1.43x slower                                                   |
| pprint_safe_repr           | 729 ms                                                                 | 1.05 sec: 1.45x slower                                                 |
| 2to3                       | 259 ms                                                                 | 376 ms: 1.45x slower                                                   |
| regex_compile              | 131 ms                                                                 | 191 ms: 1.46x slower                                                   |
| async_tree_memoization_tg  | 314 ms                                                                 | 460 ms: 1.47x slower                                                   |
| pprint_pformat             | 1.48 sec                                                               | 2.19 sec: 1.48x slower                                                 |
| subparsers                 | 22.5 ms                                                                | 33.4 ms: 1.48x slower                                                  |
| genshi_text                | 22.1 ms                                                                | 33.2 ms: 1.50x slower                                                  |
| sympy_integrate            | 20.2 ms                                                                | 30.7 ms: 1.52x slower                                                  |
| django_template            | 36.3 ms                                                                | 55.4 ms: 1.53x slower                                                  |
| sqlalchemy_imperative      | 19.2 ms                                                                | 30.0 ms: 1.57x slower                                                  |
| pyflate                    | 457 ms                                                                 | 731 ms: 1.60x slower                                                   |
| thrift                     | 744 us                                                                 | 1.20 ms: 1.61x slower                                                  |
| sqlalchemy_declarative     | 128 ms                                                                 | 207 ms: 1.62x slower                                                   |
| comprehensions             | 17.8 us                                                                | 29.1 us: 1.63x slower                                                  |
| mako                       | 11.6 ms                                                                | 19.6 ms: 1.68x slower                                                  |
| scimark_lu                 | 114 ms                                                                 | 193 ms: 1.69x slower                                                   |
| logging_format             | 7.12 us                                                                | 12.1 us: 1.69x slower                                                  |
| unpickle_pure_python       | 222 us                                                                 | 379 us: 1.70x slower                                                   |
| logging_simple             | 6.36 us                                                                | 10.9 us: 1.71x slower                                                  |
| pickle_pure_python         | 322 us                                                                 | 556 us: 1.73x slower                                                   |
| richards                   | 47.9 ms                                                                | 82.7 ms: 1.73x slower                                                  |
| hexiom                     | 6.10 ms                                                                | 10.7 ms: 1.75x slower                                                  |
| scimark_sor                | 137 ms                                                                 | 243 ms: 1.76x slower                                                   |
| sympy_str                  | 277 ms                                                                 | 493 ms: 1.78x slower                                                   |
| logging_silent             | 112 ns                                                                 | 202 ns: 1.80x slower                                                   |
| float                      | 79.2 ms                                                                | 143 ms: 1.80x slower                                                   |
| richards_super             | 54.0 ms                                                                | 99.1 ms: 1.84x slower                                                  |
| scimark_monte_carlo        | 66.4 ms                                                                | 123 ms: 1.86x slower                                                   |
| chaos                      | 60.0 ms                                                                | 112 ms: 1.87x slower                                                   |
| sqlglot_transpile          | 1.64 ms                                                                | 3.06 ms: 1.87x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                                | 2.65 ms: 2.01x slower                                                  |
| sympy_expand               | 466 ms                                                                 | 984 ms: 2.11x slower                                                   |
| raytrace                   | 272 ms                                                                 | 602 ms: 2.21x slower                                                   |
| go                         | 124 ms                                                                 | 281 ms: 2.27x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 357 ms: 2.31x slower                                                   |
| deltablue                  | 3.36 ms                                                                | 8.84 ms: 2.63x slower                                                  |
| bench_thread_pool          | 1.02 ms                                                                | 3.38 ms: 3.30x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.42x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (1) of results/bm-20241203-3.14.0a2+-6c5cec5-NOGIL/bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5.json: html5lib

- Geometric mean (including insignificant results): 1.290x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.19x