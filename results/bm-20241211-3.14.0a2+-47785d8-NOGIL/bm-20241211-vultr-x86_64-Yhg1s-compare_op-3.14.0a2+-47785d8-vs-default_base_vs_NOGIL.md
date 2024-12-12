# Results vs. default_base_vs_NOGIL

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.272x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 364 ms: 1.44x slower                                        |
| docutils       | 2.54 sec                                                               | 3.08 sec: 1.21x slower                                      |
| sphinx         | 982 ms                                                                 | 1.18 sec: 1.20x slower                                      |
| Geometric mean | (ref)                                                                  | 1.28x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                        |
| coroutines                 | 21.8 ms                                                                | 24.4 ms: 1.12x slower                                       |
| async_tree_cpu_io_mixed    | 498 ms                                                                 | 635 ms: 1.27x slower                                        |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 615 ms: 1.28x slower                                        |
| async_generators           | 358 ms                                                                 | 462 ms: 1.29x slower                                        |
| async_tree_io_tg           | 617 ms                                                                 | 818 ms: 1.33x slower                                        |
| async_tree_io              | 620 ms                                                                 | 843 ms: 1.36x slower                                        |
| async_tree_none_tg         | 257 ms                                                                 | 357 ms: 1.39x slower                                        |
| async_tree_none            | 275 ms                                                                 | 387 ms: 1.40x slower                                        |
| async_tree_memoization     | 333 ms                                                                 | 470 ms: 1.41x slower                                        |
| async_tree_memoization_tg  | 307 ms                                                                 | 449 ms: 1.46x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.29x slower                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 184 ms: 1.01x faster                                        |
| nbody          | 89.3 ms                                                                | 130 ms: 1.46x slower                                        |
| float          | 76.5 ms                                                                | 138 ms: 1.80x slower                                        |
| Geometric mean | (ref)                                                                  | 1.38x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 24.3 ms: 1.02x faster                                       |
| regex_dna      | 178 ms                                                                 | 180 ms: 1.01x slower                                        |
| regex_effbot   | 2.73 ms                                                                | 2.81 ms: 1.03x slower                                       |
| regex_compile  | 127 ms                                                                 | 179 ms: 1.41x slower                                        |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 90.7 ms                                                                | 90.3 ms: 1.00x faster                                       |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                        |
| json_loads           | 25.5 us                                                                | 28.5 us: 1.12x slower                                       |
| xml_etree_generate   | 83.7 ms                                                                | 98.9 ms: 1.18x slower                                       |
| tomli_loads          | 2.06 sec                                                               | 2.47 sec: 1.20x slower                                      |
| json_dumps           | 11.4 ms                                                                | 14.2 ms: 1.24x slower                                       |
| xml_etree_process    | 58.0 ms                                                                | 78.6 ms: 1.35x slower                                       |
| unpickle_pure_python | 213 us                                                                 | 329 us: 1.55x slower                                        |
| pickle_pure_python   | 313 us                                                                 | 497 us: 1.59x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                       |
| python_startup_no_site | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 49.6 ms                                                                | 64.3 ms: 1.29x slower                                       |
| django_template | 35.8 ms                                                                | 50.1 ms: 1.40x slower                                       |
| genshi_text     | 21.9 ms                                                                | 31.4 ms: 1.44x slower                                       |
| mako            | 11.3 ms                                                                | 17.7 ms: 1.56x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.42x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 4.38 ms                                                                | 3.18 ms: 1.38x faster                                       |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                       |
| regex_v8                   | 24.7 ms                                                                | 24.3 ms: 1.02x faster                                       |
| pidigits                   | 185 ms                                                                 | 184 ms: 1.01x faster                                        |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                        |
| xml_etree_iterparse        | 90.7 ms                                                                | 90.3 ms: 1.00x faster                                       |
| regex_dna                  | 178 ms                                                                 | 180 ms: 1.01x slower                                        |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                        |
| sqlite_synth               | 2.23 us                                                                | 2.27 us: 1.02x slower                                       |
| regex_effbot               | 2.73 ms                                                                | 2.81 ms: 1.03x slower                                       |
| json                       | 4.80 ms                                                                | 5.11 ms: 1.06x slower                                       |
| pathlib                    | 18.5 ms                                                                | 20.3 ms: 1.09x slower                                       |
| json_loads                 | 25.5 us                                                                | 28.5 us: 1.12x slower                                       |
| coroutines                 | 21.8 ms                                                                | 24.4 ms: 1.12x slower                                       |
| spectral_norm              | 106 ms                                                                 | 122 ms: 1.15x slower                                        |
| bpe_tokeniser              | 4.27 sec                                                               | 4.94 sec: 1.16x slower                                      |
| k_core                     | 2.06 sec                                                               | 2.41 sec: 1.17x slower                                      |
| mdp                        | 2.34 sec                                                               | 2.76 sec: 1.18x slower                                      |
| xml_etree_generate         | 83.7 ms                                                                | 98.9 ms: 1.18x slower                                       |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                       |
| telco                      | 7.21 ms                                                                | 8.66 ms: 1.20x slower                                       |
| tomli_loads                | 2.06 sec                                                               | 2.47 sec: 1.20x slower                                      |
| sphinx                     | 982 ms                                                                 | 1.18 sec: 1.20x slower                                      |
| docutils                   | 2.54 sec                                                               | 3.08 sec: 1.21x slower                                      |
| scimark_fft                | 326 ms                                                                 | 396 ms: 1.22x slower                                        |
| bench_mp_pool              | 88.3 ms                                                                | 108 ms: 1.22x slower                                        |
| coverage                   | 79.9 ms                                                                | 98.2 ms: 1.23x slower                                       |
| json_dumps                 | 11.4 ms                                                                | 14.2 ms: 1.24x slower                                       |
| shortest_path              | 442 ms                                                                 | 549 ms: 1.24x slower                                        |
| nqueens                    | 77.0 ms                                                                | 96.9 ms: 1.26x slower                                       |
| many_optionals             | 1.02 ms                                                                | 1.29 ms: 1.26x slower                                       |
| connected_components       | 396 ms                                                                 | 499 ms: 1.26x slower                                        |
| dulwich_log                | 75.3 ms                                                                | 95.1 ms: 1.26x slower                                       |
| fannkuch                   | 377 ms                                                                 | 479 ms: 1.27x slower                                        |
| async_tree_cpu_io_mixed    | 498 ms                                                                 | 635 ms: 1.27x slower                                        |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 615 ms: 1.28x slower                                        |
| deepcopy                   | 257 us                                                                 | 331 us: 1.29x slower                                        |
| async_generators           | 358 ms                                                                 | 462 ms: 1.29x slower                                        |
| sqlglot_normalize          | 105 ms                                                                 | 136 ms: 1.29x slower                                        |
| genshi_xml                 | 49.6 ms                                                                | 64.3 ms: 1.29x slower                                       |
| meteor_contest             | 98.7 ms                                                                | 128 ms: 1.30x slower                                        |
| sqlglot_optimize           | 53.0 ms                                                                | 68.7 ms: 1.30x slower                                       |
| typing_runtime_protocols   | 158 us                                                                 | 208 us: 1.32x slower                                        |
| crypto_pyaes               | 68.9 ms                                                                | 91.2 ms: 1.32x slower                                       |
| async_tree_io_tg           | 617 ms                                                                 | 818 ms: 1.33x slower                                        |
| deepcopy_reduce            | 2.64 us                                                                | 3.51 us: 1.33x slower                                       |
| pycparser                  | 1.12 sec                                                               | 1.51 sec: 1.35x slower                                      |
| pylint                     | 281 ms                                                                 | 380 ms: 1.35x slower                                        |
| xml_etree_process          | 58.0 ms                                                                | 78.6 ms: 1.35x slower                                       |
| async_tree_io              | 620 ms                                                                 | 843 ms: 1.36x slower                                        |
| scimark_sparse_mat_mult    | 4.31 ms                                                                | 5.88 ms: 1.37x slower                                       |
| python_startup_no_site     | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                       |
| pprint_safe_repr           | 705 ms                                                                 | 970 ms: 1.38x slower                                        |
| deepcopy_memo              | 29.2 us                                                                | 40.4 us: 1.38x slower                                       |
| pprint_pformat             | 1.45 sec                                                               | 2.01 sec: 1.39x slower                                      |
| async_tree_none_tg         | 257 ms                                                                 | 357 ms: 1.39x slower                                        |
| django_template            | 35.8 ms                                                                | 50.1 ms: 1.40x slower                                       |
| async_tree_none            | 275 ms                                                                 | 387 ms: 1.40x slower                                        |
| regex_compile              | 127 ms                                                                 | 179 ms: 1.41x slower                                        |
| async_tree_memoization     | 333 ms                                                                 | 470 ms: 1.41x slower                                        |
| genshi_text                | 21.9 ms                                                                | 31.4 ms: 1.44x slower                                       |
| 2to3                       | 253 ms                                                                 | 364 ms: 1.44x slower                                        |
| nbody                      | 89.3 ms                                                                | 130 ms: 1.46x slower                                        |
| generators                 | 27.0 ms                                                                | 39.3 ms: 1.46x slower                                       |
| subparsers                 | 21.7 ms                                                                | 31.6 ms: 1.46x slower                                       |
| async_tree_memoization_tg  | 307 ms                                                                 | 449 ms: 1.46x slower                                        |
| sympy_integrate            | 19.8 ms                                                                | 29.2 ms: 1.48x slower                                       |
| pyflate                    | 444 ms                                                                 | 666 ms: 1.50x slower                                        |
| sqlalchemy_imperative      | 19.0 ms                                                                | 29.4 ms: 1.55x slower                                       |
| unpickle_pure_python       | 213 us                                                                 | 329 us: 1.55x slower                                        |
| mako                       | 11.3 ms                                                                | 17.7 ms: 1.56x slower                                       |
| thrift                     | 734 us                                                                 | 1.16 ms: 1.58x slower                                       |
| pickle_pure_python         | 313 us                                                                 | 497 us: 1.59x slower                                        |
| comprehensions             | 17.0 us                                                                | 27.1 us: 1.60x slower                                       |
| sqlalchemy_declarative     | 126 ms                                                                 | 203 ms: 1.61x slower                                        |
| hexiom                     | 5.79 ms                                                                | 9.55 ms: 1.65x slower                                       |
| scimark_lu                 | 111 ms                                                                 | 186 ms: 1.68x slower                                        |
| scimark_sor                | 131 ms                                                                 | 221 ms: 1.69x slower                                        |
| richards                   | 45.4 ms                                                                | 78.2 ms: 1.72x slower                                       |
| sympy_str                  | 272 ms                                                                 | 472 ms: 1.74x slower                                        |
| logging_format             | 6.71 us                                                                | 11.7 us: 1.74x slower                                       |
| richards_super             | 50.8 ms                                                                | 88.5 ms: 1.74x slower                                       |
| logging_simple             | 5.96 us                                                                | 10.7 us: 1.79x slower                                       |
| float                      | 76.5 ms                                                                | 138 ms: 1.80x slower                                        |
| chaos                      | 57.6 ms                                                                | 104 ms: 1.81x slower                                        |
| scimark_monte_carlo        | 62.8 ms                                                                | 116 ms: 1.84x slower                                        |
| sqlglot_transpile          | 1.58 ms                                                                | 2.91 ms: 1.85x slower                                       |
| logging_silent             | 101 ns                                                                 | 188 ns: 1.87x slower                                        |
| sqlglot_parse              | 1.26 ms                                                                | 2.52 ms: 2.00x slower                                       |
| sympy_expand               | 456 ms                                                                 | 945 ms: 2.07x slower                                        |
| raytrace                   | 256 ms                                                                 | 559 ms: 2.18x slower                                        |
| go                         | 117 ms                                                                 | 266 ms: 2.27x slower                                        |
| sympy_sum                  | 151 ms                                                                 | 349 ms: 2.30x slower                                        |
| deltablue                  | 3.20 ms                                                                | 8.06 ms: 2.52x slower                                       |
| bench_thread_pool          | 1.02 ms                                                                | 3.40 ms: 3.32x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.39x slower                                                |
Ignored benchmarks (1) of results/bm-20241211-3.14.0a2+-47785d8-NOGIL/bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8.json: html5lib

- Geometric mean (including insignificant results): 1.272x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.19x