# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: 819a848
- commit date: 2026-04-30
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 289 ms: 1.13x slower                                                     |
| docutils       | 2.47 sec                                                               | 2.80 sec: 1.14x slower                                                   |
| html5lib       | 59.8 ms                                                                | 69.1 ms: 1.15x slower                                                    |
| sphinx         | 958 ms                                                                 | 1.08 sec: 1.13x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                 | 508 ms: 1.07x faster                                                     |
| coroutines                 | 23.9 ms                                                                | 23.9 ms: 1.00x faster                                                    |
| async_generators           | 344 ms                                                                 | 376 ms: 1.09x slower                                                     |
| async_tree_io_tg           | 570 ms                                                                 | 636 ms: 1.11x slower                                                     |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 550 ms: 1.12x slower                                                     |
| async_tree_none_tg         | 245 ms                                                                 | 285 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 566 ms: 1.17x slower                                                     |
| async_tree_io              | 568 ms                                                                 | 673 ms: 1.19x slower                                                     |
| async_tree_memoization_tg  | 303 ms                                                                 | 359 ms: 1.19x slower                                                     |
| async_tree_memoization     | 305 ms                                                                 | 379 ms: 1.24x slower                                                     |
| async_tree_none            | 245 ms                                                                 | 323 ms: 1.32x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 180 ms: 1.02x faster                                                     |
| float          | 71.4 ms                                                                | 78.6 ms: 1.10x slower                                                    |
| nbody          | 95.9 ms                                                                | 123 ms: 1.28x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 21.9 ms                                                                | 22.0 ms: 1.00x slower                                                    |
| regex_dna      | 178 ms                                                                 | 186 ms: 1.05x slower                                                     |
| regex_effbot   | 2.89 ms                                                                | 3.05 ms: 1.06x slower                                                    |
| regex_compile  | 126 ms                                                                 | 143 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                 | 134 ms: 1.03x slower                                                     |
| tomli_loads          | 1.85 sec                                                               | 1.95 sec: 1.05x slower                                                   |
| xml_etree_iterparse  | 84.2 ms                                                                | 88.8 ms: 1.06x slower                                                    |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                                    |
| pickle_pure_python   | 312 us                                                                 | 336 us: 1.08x slower                                                     |
| unpickle_pure_python | 213 us                                                                 | 236 us: 1.10x slower                                                     |
| json_dumps           | 9.57 ms                                                                | 10.8 ms: 1.13x slower                                                    |
| xml_etree_generate   | 84.7 ms                                                                | 96.0 ms: 1.13x slower                                                    |
| xml_etree_process    | 60.3 ms                                                                | 68.5 ms: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 15.3 ms: 1.23x slower                                                    |
| python_startup_no_site | 6.86 ms                                                                | 8.78 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 35.6 ms                                                                | 39.9 ms: 1.12x slower                                                    |
| mako            | 12.0 ms                                                                | 15.7 ms: 1.30x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool              | 269 ms                                                                 | 7.05 ms: 38.11x faster                                                   |
| gc_traversal               | 4.06 ms                                                                | 1.88 ms: 2.16x faster                                                    |
| create_gc_cycles           | 1.85 ms                                                                | 1.44 ms: 1.29x faster                                                    |
| sqlite_synth               | 2.21 us                                                                | 1.92 us: 1.15x faster                                                    |
| asyncio_websockets         | 544 ms                                                                 | 508 ms: 1.07x faster                                                     |
| pidigits                   | 184 ms                                                                 | 180 ms: 1.02x faster                                                     |
| json                       | 5.11 ms                                                                | 5.05 ms: 1.01x faster                                                    |
| coroutines                 | 23.9 ms                                                                | 23.9 ms: 1.00x faster                                                    |
| regex_v8                   | 21.9 ms                                                                | 22.0 ms: 1.00x slower                                                    |
| pathlib                    | 17.4 ms                                                                | 17.6 ms: 1.01x slower                                                    |
| xml_etree_parse            | 130 ms                                                                 | 134 ms: 1.03x slower                                                     |
| regex_dna                  | 178 ms                                                                 | 186 ms: 1.05x slower                                                     |
| pycparser                  | 1.07 sec                                                               | 1.13 sec: 1.05x slower                                                   |
| bpe_tokeniser              | 4.14 sec                                                               | 4.35 sec: 1.05x slower                                                   |
| tomli_loads                | 1.85 sec                                                               | 1.95 sec: 1.05x slower                                                   |
| xml_etree_iterparse        | 84.2 ms                                                                | 88.8 ms: 1.06x slower                                                    |
| regex_effbot               | 2.89 ms                                                                | 3.05 ms: 1.06x slower                                                    |
| dulwich_log                | 67.4 ms                                                                | 71.5 ms: 1.06x slower                                                    |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                                    |
| pprint_safe_repr           | 735 ms                                                                 | 791 ms: 1.08x slower                                                     |
| pickle_pure_python         | 312 us                                                                 | 336 us: 1.08x slower                                                     |
| scimark_sor                | 110 ms                                                                 | 119 ms: 1.08x slower                                                     |
| pyflate                    | 412 ms                                                                 | 449 ms: 1.09x slower                                                     |
| pprint_pformat             | 1.49 sec                                                               | 1.63 sec: 1.09x slower                                                   |
| async_generators           | 344 ms                                                                 | 376 ms: 1.09x slower                                                     |
| many_optionals             | 945 us                                                                 | 1.03 ms: 1.09x slower                                                    |
| comprehensions             | 16.0 us                                                                | 17.5 us: 1.09x slower                                                    |
| scimark_fft                | 305 ms                                                                 | 335 ms: 1.10x slower                                                     |
| deltablue                  | 3.33 ms                                                                | 3.67 ms: 1.10x slower                                                    |
| sympy_expand               | 479 ms                                                                 | 527 ms: 1.10x slower                                                     |
| telco                      | 160 ms                                                                 | 176 ms: 1.10x slower                                                     |
| float                      | 71.4 ms                                                                | 78.6 ms: 1.10x slower                                                    |
| unpickle_pure_python       | 213 us                                                                 | 236 us: 1.10x slower                                                     |
| bench_thread_pool          | 1.32 ms                                                                | 1.46 ms: 1.11x slower                                                    |
| sqlglot_v2_optimize        | 51.0 ms                                                                | 56.7 ms: 1.11x slower                                                    |
| async_tree_io_tg           | 570 ms                                                                 | 636 ms: 1.11x slower                                                     |
| django_template            | 35.6 ms                                                                | 39.9 ms: 1.12x slower                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                 | 114 ms: 1.12x slower                                                     |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 550 ms: 1.12x slower                                                     |
| 2to3                       | 257 ms                                                                 | 289 ms: 1.13x slower                                                     |
| sphinx                     | 958 ms                                                                 | 1.08 sec: 1.13x slower                                                   |
| pylint                     | 116 ms                                                                 | 131 ms: 1.13x slower                                                     |
| json_dumps                 | 9.57 ms                                                                | 10.8 ms: 1.13x slower                                                    |
| scimark_lu                 | 110 ms                                                                 | 125 ms: 1.13x slower                                                     |
| chaos                      | 55.1 ms                                                                | 62.3 ms: 1.13x slower                                                    |
| deepcopy_reduce            | 2.55 us                                                                | 2.89 us: 1.13x slower                                                    |
| xml_etree_generate         | 84.7 ms                                                                | 96.0 ms: 1.13x slower                                                    |
| deepcopy                   | 235 us                                                                 | 266 us: 1.14x slower                                                     |
| xml_etree_process          | 60.3 ms                                                                | 68.5 ms: 1.14x slower                                                    |
| docutils                   | 2.47 sec                                                               | 2.80 sec: 1.14x slower                                                   |
| regex_compile              | 126 ms                                                                 | 143 ms: 1.14x slower                                                     |
| subparsers                 | 9.12 ms                                                                | 10.4 ms: 1.14x slower                                                    |
| mdp                        | 1.16 sec                                                               | 1.32 sec: 1.14x slower                                                   |
| go                         | 107 ms                                                                 | 122 ms: 1.14x slower                                                     |
| spectral_norm              | 94.6 ms                                                                | 108 ms: 1.14x slower                                                     |
| sympy_str                  | 273 ms                                                                 | 315 ms: 1.15x slower                                                     |
| fannkuch                   | 392 ms                                                                 | 451 ms: 1.15x slower                                                     |
| deepcopy_memo              | 26.9 us                                                                | 31.0 us: 1.15x slower                                                    |
| html5lib                   | 59.8 ms                                                                | 69.1 ms: 1.15x slower                                                    |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.35 ms: 1.16x slower                                                    |
| nqueens                    | 76.2 ms                                                                | 88.1 ms: 1.16x slower                                                    |
| sympy_integrate            | 18.8 ms                                                                | 21.9 ms: 1.16x slower                                                    |
| hexiom                     | 5.69 ms                                                                | 6.62 ms: 1.16x slower                                                    |
| sqlglot_v2_transpile       | 1.47 ms                                                                | 1.71 ms: 1.16x slower                                                    |
| async_tree_none_tg         | 245 ms                                                                 | 285 ms: 1.16x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 566 ms: 1.17x slower                                                     |
| scimark_sparse_mat_mult    | 4.43 ms                                                                | 5.21 ms: 1.18x slower                                                    |
| logging_simple             | 5.87 us                                                                | 6.93 us: 1.18x slower                                                    |
| generators                 | 28.9 ms                                                                | 34.1 ms: 1.18x slower                                                    |
| logging_format             | 6.62 us                                                                | 7.82 us: 1.18x slower                                                    |
| thrift                     | 768 us                                                                 | 909 us: 1.18x slower                                                     |
| async_tree_io              | 568 ms                                                                 | 673 ms: 1.19x slower                                                     |
| async_tree_memoization_tg  | 303 ms                                                                 | 359 ms: 1.19x slower                                                     |
| k_core                     | 1.88 sec                                                               | 2.24 sec: 1.20x slower                                                   |
| raytrace                   | 251 ms                                                                 | 302 ms: 1.20x slower                                                     |
| richards_super             | 49.9 ms                                                                | 60.2 ms: 1.21x slower                                                    |
| richards                   | 43.1 ms                                                                | 52.5 ms: 1.22x slower                                                    |
| crypto_pyaes               | 72.0 ms                                                                | 88.2 ms: 1.23x slower                                                    |
| shortest_path              | 436 ms                                                                 | 535 ms: 1.23x slower                                                     |
| typing_runtime_protocols   | 158 us                                                                 | 194 us: 1.23x slower                                                     |
| python_startup             | 12.4 ms                                                                | 15.3 ms: 1.23x slower                                                    |
| async_tree_memoization     | 305 ms                                                                 | 379 ms: 1.24x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                     |
| scimark_monte_carlo        | 62.9 ms                                                                | 79.0 ms: 1.26x slower                                                    |
| connected_components       | 392 ms                                                                 | 492 ms: 1.26x slower                                                     |
| python_startup_no_site     | 6.86 ms                                                                | 8.78 ms: 1.28x slower                                                    |
| nbody                      | 95.9 ms                                                                | 123 ms: 1.28x slower                                                     |
| mako                       | 12.0 ms                                                                | 15.7 ms: 1.30x slower                                                    |
| async_tree_none            | 245 ms                                                                 | 323 ms: 1.32x slower                                                     |
| coverage                   | 81.3 ms                                                                | 110 ms: 1.35x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                             |

Benchmark hidden because not significant (1): logging_silent

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.17x