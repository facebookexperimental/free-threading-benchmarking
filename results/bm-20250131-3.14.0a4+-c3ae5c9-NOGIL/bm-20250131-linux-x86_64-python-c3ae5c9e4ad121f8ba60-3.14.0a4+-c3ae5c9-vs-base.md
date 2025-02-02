# Results vs. base

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.011x slower
- HPT reliability: 91.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg | 503 ms                                                                 | 453 ms: 1.11x faster                                                   |
| async_tree_io_tg          | 795 ms                                                                 | 742 ms: 1.07x faster                                                   |
| async_tree_memoization    | 527 ms                                                                 | 498 ms: 1.06x faster                                                   |
| async_tree_none           | 430 ms                                                                 | 413 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed   | 738 ms                                                                 | 769 ms: 1.04x slower                                                   |
| coroutines                | 33.5 ms                                                                | 35.2 ms: 1.05x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io, async_generators, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                 | 235 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 217 ms                                                                 | 205 ms: 1.06x faster                                                   |
| regex_v8       | 32.3 ms                                                                | 34.2 ms: 1.06x slower                                                  |
| regex_dna      | 281 ms                                                                 | 308 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_process    | 98.1 ms                                                                | 89.1 ms: 1.10x faster                                                  |
| json_loads           | 45.1 us                                                                | 41.9 us: 1.08x faster                                                  |
| xml_etree_parse      | 235 ms                                                                 | 223 ms: 1.06x faster                                                   |
| unpickle_pure_python | 336 us                                                                 | 356 us: 1.06x slower                                                   |
| tomli_loads          | 3.06 sec                                                               | 3.27 sec: 1.07x slower                                                 |
| json_dumps           | 16.8 ms                                                                | 18.3 ms: 1.09x slower                                                  |
| xml_etree_iterparse  | 148 ms                                                                 | 164 ms: 1.11x slower                                                   |
| pickle_pure_python   | 537 us                                                                 | 598 us: 1.11x slower                                                   |
| xml_etree_generate   | 133 ms                                                                 | 152 ms: 1.14x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 20.0 ms                                                                | 21.2 ms: 1.06x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 54.8 ms                                                                | 51.3 ms: 1.07x faster                                                  |
| mako            | 23.3 ms                                                                | 24.2 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg | 503 ms                                                                 | 453 ms: 1.11x faster                                                   |
| xml_etree_process         | 98.1 ms                                                                | 89.1 ms: 1.10x faster                                                  |
| sqlglot_normalize         | 164 ms                                                                 | 151 ms: 1.09x faster                                                   |
| pidigits                  | 255 ms                                                                 | 235 ms: 1.08x faster                                                   |
| deepcopy_reduce           | 4.77 us                                                                | 4.43 us: 1.08x faster                                                  |
| json_loads                | 45.1 us                                                                | 41.9 us: 1.08x faster                                                  |
| sqlglot_parse             | 2.30 ms                                                                | 2.14 ms: 1.07x faster                                                  |
| async_tree_io_tg          | 795 ms                                                                 | 742 ms: 1.07x faster                                                   |
| django_template           | 54.8 ms                                                                | 51.3 ms: 1.07x faster                                                  |
| regex_compile             | 217 ms                                                                 | 205 ms: 1.06x faster                                                   |
| async_tree_memoization    | 527 ms                                                                 | 498 ms: 1.06x faster                                                   |
| xml_etree_parse           | 235 ms                                                                 | 223 ms: 1.06x faster                                                   |
| go                        | 189 ms                                                                 | 179 ms: 1.05x faster                                                   |
| dulwich_log               | 107 ms                                                                 | 102 ms: 1.05x faster                                                   |
| logging_silent            | 157 ns                                                                 | 150 ns: 1.05x faster                                                   |
| async_tree_none           | 430 ms                                                                 | 413 ms: 1.04x faster                                                   |
| sqlglot_transpile         | 2.43 ms                                                                | 2.50 ms: 1.03x slower                                                  |
| pprint_safe_repr          | 1.08 sec                                                               | 1.12 sec: 1.03x slower                                                 |
| fannkuch                  | 641 ms                                                                 | 664 ms: 1.04x slower                                                   |
| mako                      | 23.3 ms                                                                | 24.2 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed   | 738 ms                                                                 | 769 ms: 1.04x slower                                                   |
| deepcopy                  | 395 us                                                                 | 415 us: 1.05x slower                                                   |
| coroutines                | 33.5 ms                                                                | 35.2 ms: 1.05x slower                                                  |
| gc_traversal              | 3.69 ms                                                                | 3.88 ms: 1.05x slower                                                  |
| sqlglot_optimize          | 82.1 ms                                                                | 86.9 ms: 1.06x slower                                                  |
| crypto_pyaes              | 118 ms                                                                 | 125 ms: 1.06x slower                                                   |
| regex_v8                  | 32.3 ms                                                                | 34.2 ms: 1.06x slower                                                  |
| pyflate                   | 733 ms                                                                 | 777 ms: 1.06x slower                                                   |
| unpickle_pure_python      | 336 us                                                                 | 356 us: 1.06x slower                                                   |
| python_startup_no_site    | 20.0 ms                                                                | 21.2 ms: 1.06x slower                                                  |
| tomli_loads               | 3.06 sec                                                               | 3.27 sec: 1.07x slower                                                 |
| deepcopy_memo             | 50.4 us                                                                | 54.0 us: 1.07x slower                                                  |
| mdp                       | 4.08 sec                                                               | 4.39 sec: 1.07x slower                                                 |
| typing_runtime_protocols  | 276 us                                                                 | 298 us: 1.08x slower                                                   |
| many_optionals            | 1.34 ms                                                                | 1.45 ms: 1.08x slower                                                  |
| json_dumps                | 16.8 ms                                                                | 18.3 ms: 1.09x slower                                                  |
| create_gc_cycles          | 2.61 ms                                                                | 2.84 ms: 1.09x slower                                                  |
| regex_dna                 | 281 ms                                                                 | 308 ms: 1.10x slower                                                   |
| spectral_norm             | 150 ms                                                                 | 165 ms: 1.10x slower                                                   |
| nqueens                   | 131 ms                                                                 | 145 ms: 1.10x slower                                                   |
| xml_etree_iterparse       | 148 ms                                                                 | 164 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult   | 8.17 ms                                                                | 9.10 ms: 1.11x slower                                                  |
| pickle_pure_python        | 537 us                                                                 | 598 us: 1.11x slower                                                   |
| sqlite_synth              | 3.38 us                                                                | 3.79 us: 1.12x slower                                                  |
| xml_etree_generate        | 133 ms                                                                 | 152 ms: 1.14x slower                                                   |
| chaos                     | 92.1 ms                                                                | 107 ms: 1.16x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (50): raytrace, thrift, pylint, async_tree_none_tg, sqlalchemy_declarative, bench_thread_pool, logging_simple, pathlib, sympy_str, nbody, async_tree_io, pprint_pformat, regex_effbot, sphinx, async_generators, sympy_integrate, genshi_xml, scimark_sor, async_tree_cpu_io_mixed_tg, python_startup, genshi_text, float, logging_format, shortest_path, connected_components, richards, html5lib, bpe_tokeniser, sympy_sum, deltablue, k_core, asyncio_websockets, meteor_contest, richards_super, sympy_expand, telco, docutils, comprehensions, generators, 2to3, coverage, pycparser, json, scimark_lu, bench_mp_pool, sqlalchemy_imperative, scimark_fft, scimark_monte_carlo, subparsers, hexiom

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 91.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x