# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 0637d48
- commit date: 2024-11-30
- overall geometric mean: 1.271x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 377 ms: 1.47x slower                                                     |
| docutils       | 2.63 sec                                                               | 3.20 sec: 1.22x slower                                                   |
| sphinx         | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 628 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 896 ms                                                                 | 865 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 658 ms: 1.01x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_io              | 856 ms                                                                 | 886 ms: 1.03x slower                                                     |
| async_tree_none_tg         | 345 ms                                                                 | 368 ms: 1.07x slower                                                     |
| async_tree_memoization_tg  | 389 ms                                                                 | 463 ms: 1.19x slower                                                     |
| async_tree_memoization     | 409 ms                                                                 | 490 ms: 1.20x slower                                                     |
| async_tree_none            | 333 ms                                                                 | 399 ms: 1.20x slower                                                     |
| async_generators           | 375 ms                                                                 | 471 ms: 1.25x slower                                                     |
| coroutines                 | 22.4 ms                                                                | 28.1 ms: 1.26x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 220 ms                                                                 | 181 ms: 1.22x faster                                                     |
| nbody          | 94.0 ms                                                                | 134 ms: 1.43x slower                                                     |
| float          | 81.5 ms                                                                | 141 ms: 1.73x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.87 ms: 1.03x slower                                                    |
| regex_dna      | 180 ms                                                                 | 187 ms: 1.04x slower                                                     |
| regex_v8       | 23.4 ms                                                                | 24.6 ms: 1.05x slower                                                    |
| regex_compile  | 132 ms                                                                 | 193 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 98.5 ms                                                                | 94.7 ms: 1.04x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 133 ms: 1.03x faster                                                     |
| json_loads           | 24.9 us                                                                | 28.3 us: 1.14x slower                                                    |
| xml_etree_generate   | 86.3 ms                                                                | 102 ms: 1.18x slower                                                     |
| json_dumps           | 11.4 ms                                                                | 14.3 ms: 1.26x slower                                                    |
| tomli_loads          | 2.15 sec                                                               | 2.72 sec: 1.26x slower                                                   |
| xml_etree_process    | 61.0 ms                                                                | 82.2 ms: 1.35x slower                                                    |
| pickle_pure_python   | 320 us                                                                 | 547 us: 1.71x slower                                                     |
| unpickle_pure_python | 217 us                                                                 | 372 us: 1.71x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.37 ms                                                                | 10.3 ms: 1.40x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.30x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 66.9 ms: 1.33x slower                                                    |
| genshi_text     | 22.3 ms                                                                | 33.9 ms: 1.52x slower                                                    |
| django_template | 36.0 ms                                                                | 55.7 ms: 1.55x slower                                                    |
| mako            | 11.8 ms                                                                | 19.8 ms: 1.68x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.51x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 220 ms                                                                 | 181 ms: 1.22x faster                                                     |
| gc_traversal               | 3.95 ms                                                                | 3.53 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 628 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 98.5 ms                                                                | 94.7 ms: 1.04x faster                                                    |
| async_tree_io_tg           | 896 ms                                                                 | 865 ms: 1.04x faster                                                     |
| create_gc_cycles           | 1.93 ms                                                                | 1.87 ms: 1.03x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 133 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 658 ms: 1.01x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| regex_effbot               | 2.78 ms                                                                | 2.87 ms: 1.03x slower                                                    |
| async_tree_io              | 856 ms                                                                 | 886 ms: 1.03x slower                                                     |
| regex_dna                  | 180 ms                                                                 | 187 ms: 1.04x slower                                                     |
| regex_v8                   | 23.4 ms                                                                | 24.6 ms: 1.05x slower                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.32 us: 1.06x slower                                                    |
| async_tree_none_tg         | 345 ms                                                                 | 368 ms: 1.07x slower                                                     |
| json                       | 4.48 ms                                                                | 5.05 ms: 1.13x slower                                                    |
| pathlib                    | 18.4 ms                                                                | 20.9 ms: 1.13x slower                                                    |
| json_loads                 | 24.9 us                                                                | 28.3 us: 1.14x slower                                                    |
| spectral_norm              | 116 ms                                                                 | 132 ms: 1.14x slower                                                     |
| xml_etree_generate         | 86.3 ms                                                                | 102 ms: 1.18x slower                                                     |
| scimark_fft                | 341 ms                                                                 | 404 ms: 1.19x slower                                                     |
| async_tree_memoization_tg  | 389 ms                                                                 | 463 ms: 1.19x slower                                                     |
| sphinx                     | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                   |
| async_tree_memoization     | 409 ms                                                                 | 490 ms: 1.20x slower                                                     |
| async_tree_none            | 333 ms                                                                 | 399 ms: 1.20x slower                                                     |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| telco                      | 7.27 ms                                                                | 8.84 ms: 1.22x slower                                                    |
| docutils                   | 2.63 sec                                                               | 3.20 sec: 1.22x slower                                                   |
| bpe_tokeniser              | 4.43 sec                                                               | 5.45 sec: 1.23x slower                                                   |
| mdp                        | 2.35 sec                                                               | 2.90 sec: 1.24x slower                                                   |
| async_generators           | 375 ms                                                                 | 471 ms: 1.25x slower                                                     |
| json_dumps                 | 11.4 ms                                                                | 14.3 ms: 1.26x slower                                                    |
| coroutines                 | 22.4 ms                                                                | 28.1 ms: 1.26x slower                                                    |
| tomli_loads                | 2.15 sec                                                               | 2.72 sec: 1.26x slower                                                   |
| coverage                   | 80.5 ms                                                                | 102 ms: 1.26x slower                                                     |
| nqueens                    | 80.1 ms                                                                | 101 ms: 1.27x slower                                                     |
| scimark_sparse_mat_mult    | 4.49 ms                                                                | 5.69 ms: 1.27x slower                                                    |
| bench_mp_pool              | 86.3 ms                                                                | 110 ms: 1.28x slower                                                     |
| shortest_path              | 444 ms                                                                 | 567 ms: 1.28x slower                                                     |
| connected_components       | 403 ms                                                                 | 518 ms: 1.28x slower                                                     |
| dulwich_log                | 75.3 ms                                                                | 98.9 ms: 1.31x slower                                                    |
| fannkuch                   | 384 ms                                                                 | 505 ms: 1.32x slower                                                     |
| generators                 | 29.0 ms                                                                | 38.4 ms: 1.32x slower                                                    |
| genshi_xml                 | 50.5 ms                                                                | 66.9 ms: 1.33x slower                                                    |
| many_optionals             | 1.02 ms                                                                | 1.36 ms: 1.33x slower                                                    |
| typing_runtime_protocols   | 160 us                                                                 | 215 us: 1.34x slower                                                     |
| meteor_contest             | 99.7 ms                                                                | 134 ms: 1.34x slower                                                     |
| deepcopy                   | 261 us                                                                 | 350 us: 1.34x slower                                                     |
| xml_etree_process          | 61.0 ms                                                                | 82.2 ms: 1.35x slower                                                    |
| sqlglot_optimize           | 53.7 ms                                                                | 74.9 ms: 1.40x slower                                                    |
| python_startup_no_site     | 7.37 ms                                                                | 10.3 ms: 1.40x slower                                                    |
| sqlglot_normalize          | 107 ms                                                                 | 150 ms: 1.40x slower                                                     |
| crypto_pyaes               | 67.7 ms                                                                | 95.2 ms: 1.41x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.59 sec: 1.41x slower                                                   |
| nbody                      | 94.0 ms                                                                | 134 ms: 1.43x slower                                                     |
| deepcopy_reduce            | 2.61 us                                                                | 3.73 us: 1.43x slower                                                    |
| regex_compile              | 132 ms                                                                 | 193 ms: 1.46x slower                                                     |
| pylint                     | 269 ms                                                                 | 394 ms: 1.47x slower                                                     |
| 2to3                       | 256 ms                                                                 | 377 ms: 1.47x slower                                                     |
| subparsers                 | 22.3 ms                                                                | 33.1 ms: 1.48x slower                                                    |
| pprint_safe_repr           | 723 ms                                                                 | 1.07 sec: 1.48x slower                                                   |
| deepcopy_memo              | 30.3 us                                                                | 45.1 us: 1.49x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.22 sec: 1.51x slower                                                   |
| genshi_text                | 22.3 ms                                                                | 33.9 ms: 1.52x slower                                                    |
| sympy_integrate            | 20.0 ms                                                                | 30.7 ms: 1.54x slower                                                    |
| django_template            | 36.0 ms                                                                | 55.7 ms: 1.55x slower                                                    |
| pyflate                    | 449 ms                                                                 | 713 ms: 1.59x slower                                                     |
| thrift                     | 743 us                                                                 | 1.20 ms: 1.61x slower                                                    |
| comprehensions             | 17.4 us                                                                | 29.0 us: 1.67x slower                                                    |
| mako                       | 11.8 ms                                                                | 19.8 ms: 1.68x slower                                                    |
| scimark_lu                 | 115 ms                                                                 | 194 ms: 1.69x slower                                                     |
| pickle_pure_python         | 320 us                                                                 | 547 us: 1.71x slower                                                     |
| unpickle_pure_python       | 217 us                                                                 | 372 us: 1.71x slower                                                     |
| float                      | 81.5 ms                                                                | 141 ms: 1.73x slower                                                     |
| richards                   | 47.4 ms                                                                | 83.2 ms: 1.76x slower                                                    |
| hexiom                     | 6.07 ms                                                                | 10.8 ms: 1.79x slower                                                    |
| logging_silent             | 108 ns                                                                 | 193 ns: 1.79x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 494 ms: 1.80x slower                                                     |
| scimark_sor                | 133 ms                                                                 | 241 ms: 1.81x slower                                                     |
| richards_super             | 53.9 ms                                                                | 98.4 ms: 1.83x slower                                                    |
| logging_format             | 6.86 us                                                                | 12.6 us: 1.83x slower                                                    |
| logging_simple             | 6.19 us                                                                | 11.4 us: 1.84x slower                                                    |
| scimark_monte_carlo        | 65.1 ms                                                                | 120 ms: 1.84x slower                                                     |
| chaos                      | 59.2 ms                                                                | 109 ms: 1.84x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 3.03 ms: 1.89x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.62 ms: 2.01x slower                                                    |
| sympy_expand               | 462 ms                                                                 | 985 ms: 2.13x slower                                                     |
| go                         | 122 ms                                                                 | 276 ms: 2.26x slower                                                     |
| raytrace                   | 264 ms                                                                 | 601 ms: 2.28x slower                                                     |
| sympy_sum                  | 153 ms                                                                 | 358 ms: 2.34x slower                                                     |
| deltablue                  | 3.31 ms                                                                | 8.66 ms: 2.62x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.40 ms: 3.31x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.39x slower                                                             |

Benchmark hidden because not significant (1): k_core
Ignored benchmarks (2) of results/bm-20241127-3.14.0a2+-58e334e/bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241130-3.14.0a2+-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48.json: html5lib

- Geometric mean (including insignificant results): 1.271x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.19x