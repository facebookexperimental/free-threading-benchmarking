# Results vs. base

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: 819a848
- commit date: 2026-04-30
- overall geometric mean: 1.006x slower
- HPT reliability: 72.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 284 ms                                                                 | 289 ms: 1.02x slower                                                     |
| docutils       | 2.62 sec                                                               | 2.80 sec: 1.07x slower                                                   |
| html5lib       | 66.6 ms                                                                | 69.1 ms: 1.04x slower                                                    |
| sphinx         | 1.04 sec                                                               | 1.08 sec: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 24.5 ms                                                                | 23.9 ms: 1.03x faster                                                    |
| async_generators           | 380 ms                                                                 | 376 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 617 ms                                                                 | 636 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed    | 540 ms                                                                 | 566 ms: 1.05x slower                                                     |
| async_tree_none_tg         | 270 ms                                                                 | 285 ms: 1.06x slower                                                     |
| async_tree_io              | 636 ms                                                                 | 673 ms: 1.06x slower                                                     |
| async_tree_memoization     | 358 ms                                                                 | 379 ms: 1.06x slower                                                     |
| async_tree_cpu_io_mixed_tg | 516 ms                                                                 | 550 ms: 1.06x slower                                                     |
| async_tree_memoization_tg  | 329 ms                                                                 | 359 ms: 1.09x slower                                                     |
| async_tree_none            | 289 ms                                                                 | 323 ms: 1.12x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 180 ms: 1.06x faster                                                     |
| nbody          | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| float          | 75.9 ms                                                                | 78.6 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                 | 143 ms: 1.00x slower                                                     |
| regex_v8       | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                                    |
| regex_dna      | 170 ms                                                                 | 186 ms: 1.10x slower                                                     |
| regex_effbot   | 2.77 ms                                                                | 3.05 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 30.4 us                                                                | 29.2 us: 1.04x faster                                                    |
| xml_etree_generate   | 97.1 ms                                                                | 96.0 ms: 1.01x faster                                                    |
| unpickle_pure_python | 238 us                                                                 | 236 us: 1.01x faster                                                     |
| pickle_pure_python   | 339 us                                                                 | 336 us: 1.01x faster                                                     |
| xml_etree_process    | 69.0 ms                                                                | 68.5 ms: 1.01x faster                                                    |
| xml_etree_parse      | 133 ms                                                                 | 134 ms: 1.00x slower                                                     |
| tomli_loads          | 1.94 sec                                                               | 1.95 sec: 1.01x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 86.8 ms                                                                | 88.8 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 9.31 ms                                                                | 8.78 ms: 1.06x faster                                                    |
| python_startup         | 15.9 ms                                                                | 15.3 ms: 1.04x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 39.7 ms                                                                | 39.9 ms: 1.01x slower                                                    |
| mako            | 15.5 ms                                                                | 15.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8+-8851a06 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 191 ms                                                                 | 180 ms: 1.06x faster                                                     |
| python_startup_no_site     | 9.31 ms                                                                | 8.78 ms: 1.06x faster                                                    |
| json                       | 5.31 ms                                                                | 5.05 ms: 1.05x faster                                                    |
| json_loads                 | 30.4 us                                                                | 29.2 us: 1.04x faster                                                    |
| python_startup             | 15.9 ms                                                                | 15.3 ms: 1.04x faster                                                    |
| scimark_lu                 | 128 ms                                                                 | 125 ms: 1.03x faster                                                     |
| coroutines                 | 24.5 ms                                                                | 23.9 ms: 1.03x faster                                                    |
| pyflate                    | 461 ms                                                                 | 449 ms: 1.03x faster                                                     |
| spectral_norm              | 111 ms                                                                 | 108 ms: 1.02x faster                                                     |
| bench_mp_pool              | 7.20 ms                                                                | 7.05 ms: 1.02x faster                                                    |
| richards                   | 53.6 ms                                                                | 52.5 ms: 1.02x faster                                                    |
| sqlglot_v2_parse           | 1.38 ms                                                                | 1.35 ms: 1.02x faster                                                    |
| crypto_pyaes               | 89.7 ms                                                                | 88.2 ms: 1.02x faster                                                    |
| scimark_sor                | 121 ms                                                                 | 119 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 803 ms                                                                 | 791 ms: 1.02x faster                                                     |
| deepcopy_reduce            | 2.93 us                                                                | 2.89 us: 1.02x faster                                                    |
| dulwich_log                | 72.6 ms                                                                | 71.5 ms: 1.01x faster                                                    |
| pprint_pformat             | 1.65 sec                                                               | 1.63 sec: 1.01x faster                                                   |
| deepcopy                   | 270 us                                                                 | 266 us: 1.01x faster                                                     |
| scimark_fft                | 339 ms                                                                 | 335 ms: 1.01x faster                                                     |
| pathlib                    | 17.8 ms                                                                | 17.6 ms: 1.01x faster                                                    |
| thrift                     | 919 us                                                                 | 909 us: 1.01x faster                                                     |
| xml_etree_generate         | 97.1 ms                                                                | 96.0 ms: 1.01x faster                                                    |
| chaos                      | 63.0 ms                                                                | 62.3 ms: 1.01x faster                                                    |
| sqlglot_v2_normalize       | 115 ms                                                                 | 114 ms: 1.01x faster                                                     |
| async_generators           | 380 ms                                                                 | 376 ms: 1.01x faster                                                     |
| unpickle_pure_python       | 238 us                                                                 | 236 us: 1.01x faster                                                     |
| fannkuch                   | 456 ms                                                                 | 451 ms: 1.01x faster                                                     |
| logging_silent             | 104 ns                                                                 | 103 ns: 1.01x faster                                                     |
| pickle_pure_python         | 339 us                                                                 | 336 us: 1.01x faster                                                     |
| sqlglot_v2_optimize        | 57.1 ms                                                                | 56.7 ms: 1.01x faster                                                    |
| nbody                      | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| coverage                   | 110 ms                                                                 | 110 ms: 1.01x faster                                                     |
| xml_etree_process          | 69.0 ms                                                                | 68.5 ms: 1.01x faster                                                    |
| sympy_expand               | 531 ms                                                                 | 527 ms: 1.01x faster                                                     |
| telco                      | 177 ms                                                                 | 176 ms: 1.01x faster                                                     |
| deepcopy_memo              | 31.2 us                                                                | 31.0 us: 1.01x faster                                                    |
| create_gc_cycles           | 1.45 ms                                                                | 1.44 ms: 1.01x faster                                                    |
| raytrace                   | 304 ms                                                                 | 302 ms: 1.01x faster                                                     |
| comprehensions             | 17.5 us                                                                | 17.5 us: 1.00x faster                                                    |
| hexiom                     | 6.64 ms                                                                | 6.62 ms: 1.00x faster                                                    |
| sympy_integrate            | 22.0 ms                                                                | 21.9 ms: 1.00x faster                                                    |
| scimark_sparse_mat_mult    | 5.22 ms                                                                | 5.21 ms: 1.00x faster                                                    |
| regex_compile              | 143 ms                                                                 | 143 ms: 1.00x slower                                                     |
| mdp                        | 1.32 sec                                                               | 1.32 sec: 1.00x slower                                                   |
| xml_etree_parse            | 133 ms                                                                 | 134 ms: 1.00x slower                                                     |
| richards_super             | 59.9 ms                                                                | 60.2 ms: 1.00x slower                                                    |
| sympy_sum                  | 179 ms                                                                 | 180 ms: 1.00x slower                                                     |
| tomli_loads                | 1.94 sec                                                               | 1.95 sec: 1.01x slower                                                   |
| k_core                     | 2.23 sec                                                               | 2.24 sec: 1.01x slower                                                   |
| connected_components       | 490 ms                                                                 | 492 ms: 1.01x slower                                                     |
| django_template            | 39.7 ms                                                                | 39.9 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                   |
| typing_runtime_protocols   | 192 us                                                                 | 194 us: 1.01x slower                                                     |
| shortest_path              | 530 ms                                                                 | 535 ms: 1.01x slower                                                     |
| nqueens                    | 87.1 ms                                                                | 88.1 ms: 1.01x slower                                                    |
| logging_simple             | 6.85 us                                                                | 6.93 us: 1.01x slower                                                    |
| mako                       | 15.5 ms                                                                | 15.7 ms: 1.01x slower                                                    |
| 2to3                       | 284 ms                                                                 | 289 ms: 1.02x slower                                                     |
| scimark_monte_carlo        | 77.5 ms                                                                | 79.0 ms: 1.02x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                    |
| xml_etree_iterparse        | 86.8 ms                                                                | 88.8 ms: 1.02x slower                                                    |
| meteor_contest             | 122 ms                                                                 | 126 ms: 1.03x slower                                                     |
| async_tree_io_tg           | 617 ms                                                                 | 636 ms: 1.03x slower                                                     |
| float                      | 75.9 ms                                                                | 78.6 ms: 1.04x slower                                                    |
| html5lib                   | 66.6 ms                                                                | 69.1 ms: 1.04x slower                                                    |
| sphinx                     | 1.04 sec                                                               | 1.08 sec: 1.04x slower                                                   |
| generators                 | 32.7 ms                                                                | 34.1 ms: 1.04x slower                                                    |
| regex_v8                   | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                                    |
| deltablue                  | 3.51 ms                                                                | 3.67 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 540 ms                                                                 | 566 ms: 1.05x slower                                                     |
| async_tree_none_tg         | 270 ms                                                                 | 285 ms: 1.06x slower                                                     |
| async_tree_io              | 636 ms                                                                 | 673 ms: 1.06x slower                                                     |
| async_tree_memoization     | 358 ms                                                                 | 379 ms: 1.06x slower                                                     |
| async_tree_cpu_io_mixed_tg | 516 ms                                                                 | 550 ms: 1.06x slower                                                     |
| docutils                   | 2.62 sec                                                               | 2.80 sec: 1.07x slower                                                   |
| gc_traversal               | 1.74 ms                                                                | 1.88 ms: 1.08x slower                                                    |
| async_tree_memoization_tg  | 329 ms                                                                 | 359 ms: 1.09x slower                                                     |
| regex_dna                  | 170 ms                                                                 | 186 ms: 1.10x slower                                                     |
| regex_effbot               | 2.77 ms                                                                | 3.05 ms: 1.10x slower                                                    |
| async_tree_none            | 289 ms                                                                 | 323 ms: 1.12x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (11): sympy_str, many_optionals, bench_thread_pool, asyncio_websockets, bpe_tokeniser, go, logging_format, sqlite_synth, subparsers, sqlglot_v2_transpile, pylint

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 72.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x