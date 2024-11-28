# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.274x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 377 ms: 1.47x slower                                                     |
| docutils       | 2.63 sec                                                               | 3.19 sec: 1.21x slower                                                   |
| sphinx         | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 627 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 896 ms                                                                 | 864 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 657 ms: 1.01x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_io              | 856 ms                                                                 | 893 ms: 1.04x slower                                                     |
| async_tree_none_tg         | 345 ms                                                                 | 367 ms: 1.06x slower                                                     |
| async_tree_memoization_tg  | 389 ms                                                                 | 461 ms: 1.18x slower                                                     |
| async_tree_none            | 333 ms                                                                 | 400 ms: 1.20x slower                                                     |
| async_tree_memoization     | 409 ms                                                                 | 491 ms: 1.20x slower                                                     |
| async_generators           | 375 ms                                                                 | 469 ms: 1.25x slower                                                     |
| coroutines                 | 22.4 ms                                                                | 28.2 ms: 1.26x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 220 ms                                                                 | 181 ms: 1.21x faster                                                     |
| nbody          | 94.0 ms                                                                | 139 ms: 1.48x slower                                                     |
| float          | 81.5 ms                                                                | 144 ms: 1.77x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.77 ms: 1.00x faster                                                    |
| regex_dna      | 180 ms                                                                 | 187 ms: 1.04x slower                                                     |
| regex_v8       | 23.4 ms                                                                | 24.9 ms: 1.07x slower                                                    |
| regex_compile  | 132 ms                                                                 | 194 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 98.5 ms                                                                | 94.8 ms: 1.04x faster                                                    |
| json_loads           | 24.9 us                                                                | 27.9 us: 1.12x slower                                                    |
| xml_etree_generate   | 86.3 ms                                                                | 102 ms: 1.19x slower                                                     |
| json_dumps           | 11.4 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| tomli_loads          | 2.15 sec                                                               | 2.75 sec: 1.28x slower                                                   |
| xml_etree_process    | 61.0 ms                                                                | 82.6 ms: 1.35x slower                                                    |
| pickle_pure_python   | 320 us                                                                 | 549 us: 1.72x slower                                                     |
| unpickle_pure_python | 217 us                                                                 | 378 us: 1.74x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.37 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 67.2 ms: 1.33x slower                                                    |
| genshi_text     | 22.3 ms                                                                | 33.6 ms: 1.51x slower                                                    |
| django_template | 36.0 ms                                                                | 55.7 ms: 1.55x slower                                                    |
| mako            | 11.8 ms                                                                | 19.8 ms: 1.68x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.51x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 220 ms                                                                 | 181 ms: 1.21x faster                                                     |
| gc_traversal               | 3.95 ms                                                                | 3.29 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 627 ms: 1.06x faster                                                     |
| create_gc_cycles           | 1.93 ms                                                                | 1.82 ms: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 98.5 ms                                                                | 94.8 ms: 1.04x faster                                                    |
| async_tree_io_tg           | 896 ms                                                                 | 864 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 657 ms: 1.01x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| regex_effbot               | 2.78 ms                                                                | 2.77 ms: 1.00x faster                                                    |
| async_tree_io              | 856 ms                                                                 | 893 ms: 1.04x slower                                                     |
| regex_dna                  | 180 ms                                                                 | 187 ms: 1.04x slower                                                     |
| sqlite_synth               | 2.20 us                                                                | 2.30 us: 1.05x slower                                                    |
| async_tree_none_tg         | 345 ms                                                                 | 367 ms: 1.06x slower                                                     |
| regex_v8                   | 23.4 ms                                                                | 24.9 ms: 1.07x slower                                                    |
| json_loads                 | 24.9 us                                                                | 27.9 us: 1.12x slower                                                    |
| pathlib                    | 18.4 ms                                                                | 20.8 ms: 1.13x slower                                                    |
| json                       | 4.48 ms                                                                | 5.07 ms: 1.13x slower                                                    |
| spectral_norm              | 116 ms                                                                 | 135 ms: 1.17x slower                                                     |
| scimark_fft                | 341 ms                                                                 | 402 ms: 1.18x slower                                                     |
| async_tree_memoization_tg  | 389 ms                                                                 | 461 ms: 1.18x slower                                                     |
| xml_etree_generate         | 86.3 ms                                                                | 102 ms: 1.19x slower                                                     |
| sphinx                     | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                   |
| async_tree_none            | 333 ms                                                                 | 400 ms: 1.20x slower                                                     |
| async_tree_memoization     | 409 ms                                                                 | 491 ms: 1.20x slower                                                     |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| docutils                   | 2.63 sec                                                               | 3.19 sec: 1.21x slower                                                   |
| telco                      | 7.27 ms                                                                | 8.95 ms: 1.23x slower                                                    |
| mdp                        | 2.35 sec                                                               | 2.91 sec: 1.24x slower                                                   |
| async_generators           | 375 ms                                                                 | 469 ms: 1.25x slower                                                     |
| bpe_tokeniser              | 4.43 sec                                                               | 5.55 sec: 1.25x slower                                                   |
| coroutines                 | 22.4 ms                                                                | 28.2 ms: 1.26x slower                                                    |
| json_dumps                 | 11.4 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| bench_mp_pool              | 86.3 ms                                                                | 110 ms: 1.27x slower                                                     |
| coverage                   | 80.5 ms                                                                | 102 ms: 1.27x slower                                                     |
| shortest_path              | 444 ms                                                                 | 565 ms: 1.27x slower                                                     |
| connected_components       | 403 ms                                                                 | 513 ms: 1.27x slower                                                     |
| nqueens                    | 80.1 ms                                                                | 103 ms: 1.28x slower                                                     |
| tomli_loads                | 2.15 sec                                                               | 2.75 sec: 1.28x slower                                                   |
| dulwich_log                | 75.3 ms                                                                | 99.8 ms: 1.33x slower                                                    |
| genshi_xml                 | 50.5 ms                                                                | 67.2 ms: 1.33x slower                                                    |
| scimark_sparse_mat_mult    | 4.49 ms                                                                | 5.99 ms: 1.33x slower                                                    |
| many_optionals             | 1.02 ms                                                                | 1.37 ms: 1.34x slower                                                    |
| typing_runtime_protocols   | 160 us                                                                 | 217 us: 1.35x slower                                                     |
| xml_etree_process          | 61.0 ms                                                                | 82.6 ms: 1.35x slower                                                    |
| generators                 | 29.0 ms                                                                | 39.4 ms: 1.36x slower                                                    |
| fannkuch                   | 384 ms                                                                 | 521 ms: 1.36x slower                                                     |
| deepcopy                   | 261 us                                                                 | 356 us: 1.36x slower                                                     |
| meteor_contest             | 99.7 ms                                                                | 136 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.37 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| sqlglot_optimize           | 53.7 ms                                                                | 75.0 ms: 1.40x slower                                                    |
| sqlglot_normalize          | 107 ms                                                                 | 150 ms: 1.41x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.60 sec: 1.42x slower                                                   |
| deepcopy_reduce            | 2.61 us                                                                | 3.76 us: 1.44x slower                                                    |
| crypto_pyaes               | 67.7 ms                                                                | 98.6 ms: 1.46x slower                                                    |
| regex_compile              | 132 ms                                                                 | 194 ms: 1.46x slower                                                     |
| pylint                     | 269 ms                                                                 | 394 ms: 1.46x slower                                                     |
| 2to3                       | 256 ms                                                                 | 377 ms: 1.47x slower                                                     |
| nbody                      | 94.0 ms                                                                | 139 ms: 1.48x slower                                                     |
| pprint_safe_repr           | 723 ms                                                                 | 1.07 sec: 1.48x slower                                                   |
| subparsers                 | 22.3 ms                                                                | 33.4 ms: 1.50x slower                                                    |
| genshi_text                | 22.3 ms                                                                | 33.6 ms: 1.51x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.22 sec: 1.51x slower                                                   |
| deepcopy_memo              | 30.3 us                                                                | 45.9 us: 1.52x slower                                                    |
| sympy_integrate            | 20.0 ms                                                                | 30.9 ms: 1.55x slower                                                    |
| django_template            | 36.0 ms                                                                | 55.7 ms: 1.55x slower                                                    |
| thrift                     | 743 us                                                                 | 1.20 ms: 1.61x slower                                                    |
| pyflate                    | 449 ms                                                                 | 741 ms: 1.65x slower                                                     |
| mako                       | 11.8 ms                                                                | 19.8 ms: 1.68x slower                                                    |
| comprehensions             | 17.4 us                                                                | 29.2 us: 1.68x slower                                                    |
| scimark_lu                 | 115 ms                                                                 | 195 ms: 1.70x slower                                                     |
| pickle_pure_python         | 320 us                                                                 | 549 us: 1.72x slower                                                     |
| unpickle_pure_python       | 217 us                                                                 | 378 us: 1.74x slower                                                     |
| richards                   | 47.4 ms                                                                | 83.6 ms: 1.76x slower                                                    |
| float                      | 81.5 ms                                                                | 144 ms: 1.77x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 495 ms: 1.80x slower                                                     |
| scimark_sor                | 133 ms                                                                 | 242 ms: 1.81x slower                                                     |
| hexiom                     | 6.07 ms                                                                | 11.0 ms: 1.82x slower                                                    |
| logging_format             | 6.86 us                                                                | 12.6 us: 1.84x slower                                                    |
| logging_simple             | 6.19 us                                                                | 11.4 us: 1.84x slower                                                    |
| richards_super             | 53.9 ms                                                                | 99.7 ms: 1.85x slower                                                    |
| logging_silent             | 108 ns                                                                 | 200 ns: 1.85x slower                                                     |
| scimark_monte_carlo        | 65.1 ms                                                                | 121 ms: 1.86x slower                                                     |
| chaos                      | 59.2 ms                                                                | 112 ms: 1.89x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 3.04 ms: 1.90x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.69 ms: 2.06x slower                                                    |
| sympy_expand               | 462 ms                                                                 | 982 ms: 2.13x slower                                                     |
| raytrace                   | 264 ms                                                                 | 599 ms: 2.27x slower                                                     |
| go                         | 122 ms                                                                 | 281 ms: 2.30x slower                                                     |
| sympy_sum                  | 153 ms                                                                 | 357 ms: 2.33x slower                                                     |
| deltablue                  | 3.31 ms                                                                | 8.80 ms: 2.66x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.38 ms: 3.30x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.39x slower                                                             |

Benchmark hidden because not significant (1): k_core
Ignored benchmarks (2) of results/bm-20241127-3.14.0a2+-58e334e/bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241128-3.14.0a2+-6e2f5fe-NOGIL/bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe.json: html5lib

- Geometric mean (including insignificant results): 1.274x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x