# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: 2e001e5dfdb655ce1fab
- machine: linux-x86_64
- commit hash: 2e001e5
- commit date: 2026-10-19
- overall geometric mean: 1.119x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                    | 304 ms: 1.19x slower                                                     |
| docutils       | 2.29 sec                                                                  | 2.98 sec: 1.30x slower                                                   |
| html5lib       | 57.1 ms                                                                   | 68.5 ms: 1.20x slower                                                    |
| sphinx         | 973 ms                                                                    | 1.14 sec: 1.17x slower                                                   |
| Geometric mean | (ref)                                                                     | 1.21x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 543 ms                                                                    | 499 ms: 1.09x faster                                                     |
| async_tree_io_tg           | 691 ms                                                                    | 705 ms: 1.02x slower                                                     |
| coroutines                 | 24.4 ms                                                                   | 26.2 ms: 1.07x slower                                                    |
| async_tree_cpu_io_mixed_tg | 533 ms                                                                    | 580 ms: 1.09x slower                                                     |
| async_tree_io              | 655 ms                                                                    | 723 ms: 1.10x slower                                                     |
| async_tree_cpu_io_mixed    | 521 ms                                                                    | 596 ms: 1.14x slower                                                     |
| async_tree_memoization_tg  | 344 ms                                                                    | 395 ms: 1.15x slower                                                     |
| async_tree_none_tg         | 280 ms                                                                    | 333 ms: 1.19x slower                                                     |
| async_tree_memoization     | 346 ms                                                                    | 416 ms: 1.20x slower                                                     |
| async_generators           | 347 ms                                                                    | 421 ms: 1.21x slower                                                     |
| async_tree_none            | 276 ms                                                                    | 337 ms: 1.22x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.12x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                    | 183 ms: 1.00x faster                                                     |
| float          | 72.1 ms                                                                   | 86.3 ms: 1.20x slower                                                    |
| nbody          | 92.4 ms                                                                   | 122 ms: 1.32x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.16x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.54 ms                                                                   | 2.92 ms: 1.15x slower                                                    |
| regex_compile  | 148 ms                                                                    | 172 ms: 1.16x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.08x slower                                                             |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                    | 143 ms: 1.01x slower                                                     |
| tomli_loads          | 1.84 sec                                                                  | 1.95 sec: 1.06x slower                                                   |
| xml_etree_iterparse  | 91.1 ms                                                                   | 97.2 ms: 1.07x slower                                                    |
| pickle_pure_python   | 310 us                                                                    | 337 us: 1.09x slower                                                     |
| json_loads           | 27.1 us                                                                   | 30.3 us: 1.12x slower                                                    |
| unpickle_pure_python | 214 us                                                                    | 240 us: 1.12x slower                                                     |
| json_dumps           | 9.09 ms                                                                   | 10.4 ms: 1.14x slower                                                    |
| xml_etree_generate   | 87.9 ms                                                                   | 104 ms: 1.18x slower                                                     |
| xml_etree_process    | 62.4 ms                                                                   | 77.6 ms: 1.24x slower                                                    |
| Geometric mean       | (ref)                                                                     | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.50 ms                                                                   | 9.64 ms: 1.29x slower                                                    |
| python_startup         | 11.4 ms                                                                   | 16.0 ms: 1.41x slower                                                    |
| Geometric mean         | (ref)                                                                     | 1.34x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 37.3 ms                                                                   | 42.6 ms: 1.14x slower                                                    |
| mako            | 11.8 ms                                                                   | 16.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                                     | 1.25x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool              | 271 ms                                                                    | 7.34 ms: 36.90x faster                                                   |
| gc_traversal               | 3.79 ms                                                                   | 1.82 ms: 2.08x faster                                                    |
| sqlite_synth               | 2.23 us                                                                   | 1.92 us: 1.16x faster                                                    |
| asyncio_websockets         | 543 ms                                                                    | 499 ms: 1.09x faster                                                     |
| create_gc_cycles           | 1.34 ms                                                                   | 1.33 ms: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                                    | 183 ms: 1.00x faster                                                     |
| xml_etree_parse            | 142 ms                                                                    | 143 ms: 1.01x slower                                                     |
| bench_thread_pool          | 1.35 ms                                                                   | 1.37 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 691 ms                                                                    | 705 ms: 1.02x slower                                                     |
| pycparser                  | 1.17 sec                                                                  | 1.20 sec: 1.03x slower                                                   |
| bpe_tokeniser              | 4.23 sec                                                                  | 4.38 sec: 1.04x slower                                                   |
| scimark_fft                | 308 ms                                                                    | 320 ms: 1.04x slower                                                     |
| pathlib                    | 17.5 ms                                                                   | 18.4 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 4.49 ms                                                                   | 4.76 ms: 1.06x slower                                                    |
| tomli_loads                | 1.84 sec                                                                  | 1.95 sec: 1.06x slower                                                   |
| scimark_lu                 | 120 ms                                                                    | 128 ms: 1.06x slower                                                     |
| xml_etree_iterparse        | 91.1 ms                                                                   | 97.2 ms: 1.07x slower                                                    |
| coroutines                 | 24.4 ms                                                                   | 26.2 ms: 1.07x slower                                                    |
| k_core                     | 2.07 sec                                                                  | 2.25 sec: 1.09x slower                                                   |
| dulwich_log                | 66.3 ms                                                                   | 71.9 ms: 1.09x slower                                                    |
| telco                      | 164 ms                                                                    | 178 ms: 1.09x slower                                                     |
| pickle_pure_python         | 310 us                                                                    | 337 us: 1.09x slower                                                     |
| async_tree_cpu_io_mixed_tg | 533 ms                                                                    | 580 ms: 1.09x slower                                                     |
| json                       | 4.93 ms                                                                   | 5.37 ms: 1.09x slower                                                    |
| pyflate                    | 398 ms                                                                    | 436 ms: 1.09x slower                                                     |
| scimark_sor                | 109 ms                                                                    | 120 ms: 1.10x slower                                                     |
| chaos                      | 54.4 ms                                                                   | 59.9 ms: 1.10x slower                                                    |
| logging_silent             | 96.5 ns                                                                   | 106 ns: 1.10x slower                                                     |
| async_tree_io              | 655 ms                                                                    | 723 ms: 1.10x slower                                                     |
| spectral_norm              | 91.3 ms                                                                   | 101 ms: 1.11x slower                                                     |
| many_optionals             | 887 us                                                                    | 989 us: 1.12x slower                                                     |
| pprint_safe_repr           | 734 ms                                                                    | 820 ms: 1.12x slower                                                     |
| json_loads                 | 27.1 us                                                                   | 30.3 us: 1.12x slower                                                    |
| unpickle_pure_python       | 214 us                                                                    | 240 us: 1.12x slower                                                     |
| pprint_pformat             | 1.49 sec                                                                  | 1.69 sec: 1.13x slower                                                   |
| logging_simple             | 6.22 us                                                                   | 7.06 us: 1.13x slower                                                    |
| deltablue                  | 3.31 ms                                                                   | 3.76 ms: 1.14x slower                                                    |
| go                         | 105 ms                                                                    | 119 ms: 1.14x slower                                                     |
| sqlglot_v2_normalize       | 102 ms                                                                    | 116 ms: 1.14x slower                                                     |
| json_dumps                 | 9.09 ms                                                                   | 10.4 ms: 1.14x slower                                                    |
| raytrace                   | 256 ms                                                                    | 293 ms: 1.14x slower                                                     |
| async_tree_cpu_io_mixed    | 521 ms                                                                    | 596 ms: 1.14x slower                                                     |
| django_template            | 37.3 ms                                                                   | 42.6 ms: 1.14x slower                                                    |
| async_tree_memoization_tg  | 344 ms                                                                    | 395 ms: 1.15x slower                                                     |
| sqlglot_v2_optimize        | 50.7 ms                                                                   | 58.3 ms: 1.15x slower                                                    |
| regex_effbot               | 2.54 ms                                                                   | 2.92 ms: 1.15x slower                                                    |
| logging_format             | 6.91 us                                                                   | 7.96 us: 1.15x slower                                                    |
| comprehensions             | 15.9 us                                                                   | 18.4 us: 1.16x slower                                                    |
| generators                 | 29.5 ms                                                                   | 34.3 ms: 1.16x slower                                                    |
| regex_compile              | 148 ms                                                                    | 172 ms: 1.16x slower                                                     |
| nqueens                    | 75.8 ms                                                                   | 88.2 ms: 1.16x slower                                                    |
| subparsers                 | 8.86 ms                                                                   | 10.4 ms: 1.17x slower                                                    |
| hexiom                     | 5.67 ms                                                                   | 6.65 ms: 1.17x slower                                                    |
| sphinx                     | 973 ms                                                                    | 1.14 sec: 1.17x slower                                                   |
| xml_etree_generate         | 87.9 ms                                                                   | 104 ms: 1.18x slower                                                     |
| deepcopy                   | 230 us                                                                    | 273 us: 1.18x slower                                                     |
| sympy_expand               | 476 ms                                                                    | 564 ms: 1.19x slower                                                     |
| deepcopy_reduce            | 2.55 us                                                                   | 3.03 us: 1.19x slower                                                    |
| sympy_integrate            | 19.2 ms                                                                   | 22.8 ms: 1.19x slower                                                    |
| async_tree_none_tg         | 280 ms                                                                    | 333 ms: 1.19x slower                                                     |
| 2to3                       | 255 ms                                                                    | 304 ms: 1.19x slower                                                     |
| richards                   | 44.5 ms                                                                   | 53.0 ms: 1.19x slower                                                    |
| thrift                     | 793 us                                                                    | 947 us: 1.19x slower                                                     |
| richards_super             | 50.7 ms                                                                   | 60.5 ms: 1.19x slower                                                    |
| sympy_str                  | 281 ms                                                                    | 336 ms: 1.20x slower                                                     |
| float                      | 72.1 ms                                                                   | 86.3 ms: 1.20x slower                                                    |
| html5lib                   | 57.1 ms                                                                   | 68.5 ms: 1.20x slower                                                    |
| async_tree_memoization     | 346 ms                                                                    | 416 ms: 1.20x slower                                                     |
| pylint                     | 112 ms                                                                    | 135 ms: 1.20x slower                                                     |
| shortest_path              | 438 ms                                                                    | 529 ms: 1.21x slower                                                     |
| sympy_sum                  | 158 ms                                                                    | 191 ms: 1.21x slower                                                     |
| async_generators           | 347 ms                                                                    | 421 ms: 1.21x slower                                                     |
| scimark_monte_carlo        | 62.8 ms                                                                   | 76.2 ms: 1.21x slower                                                    |
| deepcopy_memo              | 27.3 us                                                                   | 33.2 us: 1.22x slower                                                    |
| sqlglot_v2_transpile       | 1.44 ms                                                                   | 1.76 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 120 us                                                                    | 147 us: 1.22x slower                                                     |
| async_tree_none            | 276 ms                                                                    | 337 ms: 1.22x slower                                                     |
| meteor_contest             | 102 ms                                                                    | 126 ms: 1.23x slower                                                     |
| sqlglot_v2_parse           | 1.15 ms                                                                   | 1.42 ms: 1.24x slower                                                    |
| xml_etree_process          | 62.4 ms                                                                   | 77.6 ms: 1.24x slower                                                    |
| connected_components       | 395 ms                                                                    | 492 ms: 1.24x slower                                                     |
| fannkuch                   | 372 ms                                                                    | 465 ms: 1.25x slower                                                     |
| mdp                        | 1.13 sec                                                                  | 1.41 sec: 1.25x slower                                                   |
| python_startup_no_site     | 7.50 ms                                                                   | 9.64 ms: 1.29x slower                                                    |
| docutils                   | 2.29 sec                                                                  | 2.98 sec: 1.30x slower                                                   |
| nbody                      | 92.4 ms                                                                   | 122 ms: 1.32x slower                                                     |
| crypto_pyaes               | 66.4 ms                                                                   | 87.6 ms: 1.32x slower                                                    |
| mako                       | 11.8 ms                                                                   | 16.0 ms: 1.36x slower                                                    |
| python_startup             | 11.4 ms                                                                   | 16.0 ms: 1.41x slower                                                    |
| coverage                   | 82.9 ms                                                                   | 120 ms: 1.45x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.09x slower                                                             |

Benchmark hidden because not significant (2): regex_v8, regex_dna

- Geometric mean (including insignificant results): 1.119x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.25x