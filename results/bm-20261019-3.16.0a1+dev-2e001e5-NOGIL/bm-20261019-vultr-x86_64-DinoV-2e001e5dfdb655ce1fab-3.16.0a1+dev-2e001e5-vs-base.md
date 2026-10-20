# Results vs. base

- fork: DinoV
- ref: 2e001e5dfdb655ce1fab
- machine: linux-x86_64
- commit hash: 2e001e5
- commit date: 2026-10-19
- overall geometric mean: 1.011x slower
- HPT reliability: 99.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 293 ms                                                                    | 304 ms: 1.04x slower                                                     |
| docutils       | 2.88 sec                                                                  | 2.98 sec: 1.04x slower                                                   |
| html5lib       | 67.4 ms                                                                   | 68.5 ms: 1.02x slower                                                    |
| sphinx         | 1.10 sec                                                                  | 1.14 sec: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 404 ms                                                                    | 395 ms: 1.02x faster                                                     |
| async_tree_none            | 344 ms                                                                    | 337 ms: 1.02x faster                                                     |
| async_tree_memoization     | 425 ms                                                                    | 416 ms: 1.02x faster                                                     |
| asyncio_websockets         | 509 ms                                                                    | 499 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 605 ms                                                                    | 596 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 586 ms                                                                    | 580 ms: 1.01x faster                                                     |
| async_tree_io              | 718 ms                                                                    | 723 ms: 1.01x slower                                                     |
| coroutines                 | 25.9 ms                                                                   | 26.2 ms: 1.01x slower                                                    |
| async_generators           | 415 ms                                                                    | 421 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.01x faster                                                             |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 180 ms                                                                    | 183 ms: 1.02x slower                                                     |
| float          | 83.5 ms                                                                   | 86.3 ms: 1.03x slower                                                    |
| nbody          | 116 ms                                                                    | 122 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                    | 172 ms: 1.01x slower                                                     |
| regex_dna      | 174 ms                                                                    | 177 ms: 1.02x slower                                                     |
| regex_v8       | 20.7 ms                                                                   | 21.2 ms: 1.03x slower                                                    |
| regex_effbot   | 2.75 ms                                                                   | 2.92 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 30.5 us                                                                   | 30.3 us: 1.01x faster                                                    |
| unpickle_pure_python | 239 us                                                                    | 240 us: 1.00x slower                                                     |
| xml_etree_iterparse  | 96.4 ms                                                                   | 97.2 ms: 1.01x slower                                                    |
| pickle_pure_python   | 333 us                                                                    | 337 us: 1.01x slower                                                     |
| json_dumps           | 10.2 ms                                                                   | 10.4 ms: 1.01x slower                                                    |
| xml_etree_generate   | 102 ms                                                                    | 104 ms: 1.02x slower                                                     |
| xml_etree_process    | 75.4 ms                                                                   | 77.6 ms: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 16.1 ms                                                                   | 16.0 ms: 1.01x faster                                                    |
| python_startup_no_site | 9.56 ms                                                                   | 9.64 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                     | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1+dev-415ebff | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_thread_pool          | 1.64 ms                                                                   | 1.37 ms: 1.20x faster                                                    |
| scimark_sparse_mat_mult    | 4.91 ms                                                                   | 4.76 ms: 1.03x faster                                                    |
| spectral_norm              | 105 ms                                                                    | 101 ms: 1.03x faster                                                     |
| logging_silent             | 110 ns                                                                    | 106 ns: 1.03x faster                                                     |
| async_tree_memoization_tg  | 404 ms                                                                    | 395 ms: 1.02x faster                                                     |
| async_tree_none            | 344 ms                                                                    | 337 ms: 1.02x faster                                                     |
| async_tree_memoization     | 425 ms                                                                    | 416 ms: 1.02x faster                                                     |
| asyncio_websockets         | 509 ms                                                                    | 499 ms: 1.02x faster                                                     |
| scimark_lu                 | 130 ms                                                                    | 128 ms: 1.02x faster                                                     |
| scimark_fft                | 326 ms                                                                    | 320 ms: 1.02x faster                                                     |
| scimark_sor                | 122 ms                                                                    | 120 ms: 1.02x faster                                                     |
| json                       | 5.45 ms                                                                   | 5.37 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 605 ms                                                                    | 596 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 586 ms                                                                    | 580 ms: 1.01x faster                                                     |
| richards_super             | 61.0 ms                                                                   | 60.5 ms: 1.01x faster                                                    |
| json_loads                 | 30.5 us                                                                   | 30.3 us: 1.01x faster                                                    |
| richards                   | 53.4 ms                                                                   | 53.0 ms: 1.01x faster                                                    |
| shortest_path              | 533 ms                                                                    | 529 ms: 1.01x faster                                                     |
| pyflate                    | 438 ms                                                                    | 436 ms: 1.01x faster                                                     |
| go                         | 120 ms                                                                    | 119 ms: 1.01x faster                                                     |
| python_startup             | 16.1 ms                                                                   | 16.0 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.40 sec                                                                  | 4.38 sec: 1.00x faster                                                   |
| unpickle_pure_python       | 239 us                                                                    | 240 us: 1.00x slower                                                     |
| pprint_pformat             | 1.68 sec                                                                  | 1.69 sec: 1.01x slower                                                   |
| async_tree_io              | 718 ms                                                                    | 723 ms: 1.01x slower                                                     |
| crypto_pyaes               | 87.0 ms                                                                   | 87.6 ms: 1.01x slower                                                    |
| comprehensions             | 18.2 us                                                                   | 18.4 us: 1.01x slower                                                    |
| logging_simple             | 7.00 us                                                                   | 7.06 us: 1.01x slower                                                    |
| xml_etree_iterparse        | 96.4 ms                                                                   | 97.2 ms: 1.01x slower                                                    |
| nqueens                    | 87.4 ms                                                                   | 88.2 ms: 1.01x slower                                                    |
| regex_compile              | 170 ms                                                                    | 172 ms: 1.01x slower                                                     |
| python_startup_no_site     | 9.56 ms                                                                   | 9.64 ms: 1.01x slower                                                    |
| pprint_safe_repr           | 812 ms                                                                    | 820 ms: 1.01x slower                                                     |
| subparsers                 | 10.3 ms                                                                   | 10.4 ms: 1.01x slower                                                    |
| generators                 | 33.9 ms                                                                   | 34.3 ms: 1.01x slower                                                    |
| connected_components       | 487 ms                                                                    | 492 ms: 1.01x slower                                                     |
| telco                      | 176 ms                                                                    | 178 ms: 1.01x slower                                                     |
| coroutines                 | 25.9 ms                                                                   | 26.2 ms: 1.01x slower                                                    |
| async_generators           | 415 ms                                                                    | 421 ms: 1.01x slower                                                     |
| pickle_pure_python         | 333 us                                                                    | 337 us: 1.01x slower                                                     |
| json_dumps                 | 10.2 ms                                                                   | 10.4 ms: 1.01x slower                                                    |
| many_optionals             | 975 us                                                                    | 989 us: 1.01x slower                                                     |
| hexiom                     | 6.55 ms                                                                   | 6.65 ms: 1.01x slower                                                    |
| html5lib                   | 67.4 ms                                                                   | 68.5 ms: 1.02x slower                                                    |
| pidigits                   | 180 ms                                                                    | 183 ms: 1.02x slower                                                     |
| deepcopy_memo              | 32.6 us                                                                   | 33.2 us: 1.02x slower                                                    |
| meteor_contest             | 123 ms                                                                    | 126 ms: 1.02x slower                                                     |
| regex_dna                  | 174 ms                                                                    | 177 ms: 1.02x slower                                                     |
| fannkuch                   | 456 ms                                                                    | 465 ms: 1.02x slower                                                     |
| xml_etree_generate         | 102 ms                                                                    | 104 ms: 1.02x slower                                                     |
| dulwich_log                | 70.2 ms                                                                   | 71.9 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile       | 1.72 ms                                                                   | 1.76 ms: 1.02x slower                                                    |
| regex_v8                   | 20.7 ms                                                                   | 21.2 ms: 1.03x slower                                                    |
| typing_runtime_protocols   | 143 us                                                                    | 147 us: 1.03x slower                                                     |
| deepcopy                   | 266 us                                                                    | 273 us: 1.03x slower                                                     |
| pathlib                    | 18.0 ms                                                                   | 18.4 ms: 1.03x slower                                                    |
| sqlglot_v2_parse           | 1.39 ms                                                                   | 1.42 ms: 1.03x slower                                                    |
| gc_traversal               | 1.77 ms                                                                   | 1.82 ms: 1.03x slower                                                    |
| sqlglot_v2_optimize        | 56.7 ms                                                                   | 58.3 ms: 1.03x slower                                                    |
| xml_etree_process          | 75.4 ms                                                                   | 77.6 ms: 1.03x slower                                                    |
| sqlglot_v2_normalize       | 113 ms                                                                    | 116 ms: 1.03x slower                                                     |
| deepcopy_reduce            | 2.94 us                                                                   | 3.03 us: 1.03x slower                                                    |
| float                      | 83.5 ms                                                                   | 86.3 ms: 1.03x slower                                                    |
| sphinx                     | 1.10 sec                                                                  | 1.14 sec: 1.03x slower                                                   |
| coverage                   | 116 ms                                                                    | 120 ms: 1.03x slower                                                     |
| docutils                   | 2.88 sec                                                                  | 2.98 sec: 1.04x slower                                                   |
| 2to3                       | 293 ms                                                                    | 304 ms: 1.04x slower                                                     |
| thrift                     | 909 us                                                                    | 947 us: 1.04x slower                                                     |
| sympy_integrate            | 21.9 ms                                                                   | 22.8 ms: 1.04x slower                                                    |
| pycparser                  | 1.15 sec                                                                  | 1.20 sec: 1.05x slower                                                   |
| nbody                      | 116 ms                                                                    | 122 ms: 1.05x slower                                                     |
| sympy_str                  | 318 ms                                                                    | 336 ms: 1.06x slower                                                     |
| sympy_sum                  | 180 ms                                                                    | 191 ms: 1.06x slower                                                     |
| regex_effbot               | 2.75 ms                                                                   | 2.92 ms: 1.06x slower                                                    |
| sympy_expand               | 531 ms                                                                    | 564 ms: 1.06x slower                                                     |
| mdp                        | 1.31 sec                                                                  | 1.41 sec: 1.08x slower                                                   |
| bench_mp_pool              | 6.73 ms                                                                   | 7.34 ms: 1.09x slower                                                    |
| Geometric mean             | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (15): async_tree_none_tg, create_gc_cycles, deltablue, tomli_loads, raytrace, sqlite_synth, mako, k_core, chaos, scimark_monte_carlo, logging_format, async_tree_io_tg, xml_etree_parse, django_template, pylint

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 99.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x