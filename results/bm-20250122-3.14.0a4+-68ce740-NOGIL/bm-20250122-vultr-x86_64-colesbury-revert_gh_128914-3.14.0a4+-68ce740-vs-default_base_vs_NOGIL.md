# Results vs. default_base_vs_NOGIL

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.130x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 305 ms: 1.19x slower                                                  |
| docutils       | 2.60 sec                                                               | 2.82 sec: 1.09x slower                                                |
| sphinx         | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 260 ms                                                                 | 241 ms: 1.08x faster                                                  |
| async_tree_io_tg           | 618 ms                                                                 | 579 ms: 1.07x faster                                                  |
| async_tree_io              | 612 ms                                                                 | 601 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 311 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 505 ms: 1.05x slower                                                  |
| async_tree_none            | 267 ms                                                                 | 283 ms: 1.06x slower                                                  |
| coroutines                 | 22.0 ms                                                                | 23.4 ms: 1.06x slower                                                 |
| async_tree_memoization     | 324 ms                                                                 | 346 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 539 ms: 1.09x slower                                                  |
| async_generators           | 322 ms                                                                 | 368 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 195 ms: 1.01x slower                                                  |
| float          | 70.9 ms                                                                | 77.1 ms: 1.09x slower                                                 |
| nbody          | 90.7 ms                                                                | 136 ms: 1.50x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.72 ms                                                                | 2.84 ms: 1.04x slower                                                 |
| regex_dna      | 173 ms                                                                 | 186 ms: 1.07x slower                                                  |
| regex_compile  | 129 ms                                                                 | 152 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 87.8 ms: 1.04x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| unpickle_pure_python | 226 us                                                                 | 250 us: 1.11x slower                                                  |
| json_loads           | 27.6 us                                                                | 30.8 us: 1.11x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 12.9 ms: 1.13x slower                                                 |
| xml_etree_process    | 60.6 ms                                                                | 69.5 ms: 1.15x slower                                                 |
| pickle_pure_python   | 322 us                                                                 | 373 us: 1.16x slower                                                  |
| xml_etree_generate   | 83.3 ms                                                                | 97.2 ms: 1.17x slower                                                 |
| tomli_loads          | 1.96 sec                                                               | 2.37 sec: 1.21x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| python_startup_no_site | 7.43 ms                                                                | 9.54 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.4 ms                                                                | 43.0 ms: 1.18x slower                                                 |
| genshi_xml      | 49.9 ms                                                                | 59.9 ms: 1.20x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.5 ms: 1.27x slower                                                 |
| mako            | 11.8 ms                                                                | 16.0 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 1.82 ms                                                                | 1.36 ms: 1.34x faster                                                 |
| gc_traversal               | 4.18 ms                                                                | 3.34 ms: 1.25x faster                                                 |
| sqlite_synth               | 2.21 us                                                                | 2.04 us: 1.08x faster                                                 |
| async_tree_none_tg         | 260 ms                                                                 | 241 ms: 1.08x faster                                                  |
| async_tree_io_tg           | 618 ms                                                                 | 579 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 91.5 ms                                                                | 87.8 ms: 1.04x faster                                                 |
| async_tree_io              | 612 ms                                                                 | 601 ms: 1.02x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| pidigits                   | 192 ms                                                                 | 195 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 311 ms: 1.02x slower                                                  |
| python_startup             | 14.6 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| regex_effbot               | 2.72 ms                                                                | 2.84 ms: 1.04x slower                                                 |
| pycparser                  | 1.14 sec                                                               | 1.19 sec: 1.05x slower                                                |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 505 ms: 1.05x slower                                                  |
| bench_mp_pool              | 89.0 ms                                                                | 94.3 ms: 1.06x slower                                                 |
| async_tree_none            | 267 ms                                                                 | 283 ms: 1.06x slower                                                  |
| coroutines                 | 22.0 ms                                                                | 23.4 ms: 1.06x slower                                                 |
| dulwich_log                | 77.0 ms                                                                | 82.4 ms: 1.07x slower                                                 |
| json                       | 4.98 ms                                                                | 5.33 ms: 1.07x slower                                                 |
| async_tree_memoization     | 324 ms                                                                 | 346 ms: 1.07x slower                                                  |
| regex_dna                  | 173 ms                                                                 | 186 ms: 1.07x slower                                                  |
| float                      | 70.9 ms                                                                | 77.1 ms: 1.09x slower                                                 |
| docutils                   | 2.60 sec                                                               | 2.82 sec: 1.09x slower                                                |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 539 ms: 1.09x slower                                                  |
| logging_silent             | 103 ns                                                                 | 113 ns: 1.10x slower                                                  |
| unpickle_pure_python       | 226 us                                                                 | 250 us: 1.11x slower                                                  |
| bpe_tokeniser              | 4.25 sec                                                               | 4.74 sec: 1.11x slower                                                |
| json_loads                 | 27.6 us                                                                | 30.8 us: 1.11x slower                                                 |
| pylint                     | 282 ms                                                                 | 318 ms: 1.13x slower                                                  |
| many_optionals             | 1.05 ms                                                                | 1.18 ms: 1.13x slower                                                 |
| logging_simple             | 6.50 us                                                                | 7.34 us: 1.13x slower                                                 |
| json_dumps                 | 11.4 ms                                                                | 12.9 ms: 1.13x slower                                                 |
| sphinx                     | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| k_core                     | 2.05 sec                                                               | 2.32 sec: 1.13x slower                                                |
| subparsers                 | 22.4 ms                                                                | 25.5 ms: 1.14x slower                                                 |
| async_generators           | 322 ms                                                                 | 368 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 105 ms                                                                 | 121 ms: 1.15x slower                                                  |
| xml_etree_process          | 60.6 ms                                                                | 69.5 ms: 1.15x slower                                                 |
| generators                 | 27.3 ms                                                                | 31.4 ms: 1.15x slower                                                 |
| sqlglot_optimize           | 52.9 ms                                                                | 61.0 ms: 1.15x slower                                                 |
| pickle_pure_python         | 322 us                                                                 | 373 us: 1.16x slower                                                  |
| logging_format             | 7.21 us                                                                | 8.37 us: 1.16x slower                                                 |
| scimark_sor                | 113 ms                                                                 | 132 ms: 1.16x slower                                                  |
| xml_etree_generate         | 83.3 ms                                                                | 97.2 ms: 1.17x slower                                                 |
| go                         | 118 ms                                                                 | 138 ms: 1.17x slower                                                  |
| mdp                        | 2.31 sec                                                               | 2.70 sec: 1.17x slower                                                |
| regex_compile              | 129 ms                                                                 | 152 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 704 ms                                                                 | 830 ms: 1.18x slower                                                  |
| django_template            | 36.4 ms                                                                | 43.0 ms: 1.18x slower                                                 |
| telco                      | 7.20 ms                                                                | 8.51 ms: 1.18x slower                                                 |
| sympy_expand               | 463 ms                                                                 | 549 ms: 1.19x slower                                                  |
| spectral_norm              | 94.0 ms                                                                | 112 ms: 1.19x slower                                                  |
| 2to3                       | 256 ms                                                                 | 305 ms: 1.19x slower                                                  |
| sympy_sum                  | 156 ms                                                                 | 186 ms: 1.20x slower                                                  |
| thrift                     | 749 us                                                                 | 898 us: 1.20x slower                                                  |
| pprint_pformat             | 1.43 sec                                                               | 1.72 sec: 1.20x slower                                                |
| genshi_xml                 | 49.9 ms                                                                | 59.9 ms: 1.20x slower                                                 |
| sympy_integrate            | 20.0 ms                                                                | 24.2 ms: 1.20x slower                                                 |
| pyflate                    | 411 ms                                                                 | 496 ms: 1.21x slower                                                  |
| tomli_loads                | 1.96 sec                                                               | 2.37 sec: 1.21x slower                                                |
| deepcopy                   | 259 us                                                                 | 314 us: 1.21x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                                  |
| deepcopy_reduce            | 2.66 us                                                                | 3.23 us: 1.21x slower                                                 |
| sympy_str                  | 275 ms                                                                 | 335 ms: 1.22x slower                                                  |
| coverage                   | 80.0 ms                                                                | 97.5 ms: 1.22x slower                                                 |
| sqlalchemy_imperative      | 19.8 ms                                                                | 24.4 ms: 1.23x slower                                                 |
| raytrace                   | 266 ms                                                                 | 329 ms: 1.23x slower                                                  |
| hexiom                     | 5.90 ms                                                                | 7.29 ms: 1.24x slower                                                 |
| chaos                      | 56.0 ms                                                                | 69.3 ms: 1.24x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.6 us: 1.25x slower                                                 |
| nqueens                    | 77.9 ms                                                                | 97.1 ms: 1.25x slower                                                 |
| scimark_fft                | 312 ms                                                                 | 389 ms: 1.25x slower                                                  |
| sqlalchemy_declarative     | 130 ms                                                                 | 163 ms: 1.25x slower                                                  |
| deepcopy_memo              | 30.6 us                                                                | 38.4 us: 1.26x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                                | 1.96 ms: 1.26x slower                                                 |
| connected_components       | 390 ms                                                                 | 490 ms: 1.26x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.26x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 27.5 ms: 1.27x slower                                                 |
| shortest_path              | 427 ms                                                                 | 542 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 158 us                                                                 | 201 us: 1.27x slower                                                  |
| python_startup_no_site     | 7.43 ms                                                                | 9.54 ms: 1.28x slower                                                 |
| fannkuch                   | 374 ms                                                                 | 481 ms: 1.29x slower                                                  |
| scimark_monte_carlo        | 63.0 ms                                                                | 82.0 ms: 1.30x slower                                                 |
| scimark_sparse_mat_mult    | 4.17 ms                                                                | 5.48 ms: 1.31x slower                                                 |
| crypto_pyaes               | 67.8 ms                                                                | 89.2 ms: 1.32x slower                                                 |
| meteor_contest             | 98.7 ms                                                                | 130 ms: 1.32x slower                                                  |
| richards                   | 42.4 ms                                                                | 56.5 ms: 1.33x slower                                                 |
| richards_super             | 48.5 ms                                                                | 64.8 ms: 1.34x slower                                                 |
| mako                       | 11.8 ms                                                                | 16.0 ms: 1.35x slower                                                 |
| deltablue                  | 3.20 ms                                                                | 4.58 ms: 1.43x slower                                                 |
| nbody                      | 90.7 ms                                                                | 136 ms: 1.50x slower                                                  |
| bench_thread_pool          | 1.04 ms                                                                | 3.31 ms: 3.19x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, pathlib
Ignored benchmarks (1) of results/bm-20250122-3.14.0a4+-68ce740-NOGIL/bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740.json: html5lib

- Geometric mean (including insignificant results): 1.130x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x