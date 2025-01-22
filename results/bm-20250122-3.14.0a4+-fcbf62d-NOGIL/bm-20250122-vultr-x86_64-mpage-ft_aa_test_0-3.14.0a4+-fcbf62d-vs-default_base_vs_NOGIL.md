# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: ft_aa_test_0
- machine: linux-x86_64
- commit hash: fcbf62d
- commit date: 2025-01-22
- overall geometric mean: 1.152x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 314 ms: 1.22x slower                                          |
| docutils       | 2.60 sec                                                               | 2.86 sec: 1.10x slower                                        |
| sphinx         | 993 ms                                                                 | 1.14 sec: 1.15x slower                                        |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 618 ms                                                                 | 582 ms: 1.06x faster                                          |
| async_tree_none_tg         | 260 ms                                                                 | 246 ms: 1.05x faster                                          |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                          |
| async_tree_memoization_tg  | 306 ms                                                                 | 318 ms: 1.04x slower                                          |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 502 ms: 1.04x slower                                          |
| async_tree_none            | 267 ms                                                                 | 289 ms: 1.08x slower                                          |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 537 ms: 1.09x slower                                          |
| async_tree_memoization     | 324 ms                                                                 | 357 ms: 1.10x slower                                          |
| coroutines                 | 22.0 ms                                                                | 25.4 ms: 1.16x slower                                         |
| async_generators           | 322 ms                                                                 | 376 ms: 1.17x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                  |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 196 ms: 1.02x slower                                          |
| float          | 70.9 ms                                                                | 78.0 ms: 1.10x slower                                         |
| nbody          | 90.7 ms                                                                | 141 ms: 1.55x slower                                          |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                         |
| regex_effbot   | 2.72 ms                                                                | 2.88 ms: 1.06x slower                                         |
| regex_dna      | 173 ms                                                                 | 183 ms: 1.06x slower                                          |
| regex_compile  | 129 ms                                                                 | 160 ms: 1.24x slower                                          |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 87.9 ms: 1.04x faster                                         |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                          |
| json_loads           | 27.6 us                                                                | 30.6 us: 1.11x slower                                         |
| json_dumps           | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                         |
| xml_etree_generate   | 83.3 ms                                                                | 99.0 ms: 1.19x slower                                         |
| unpickle_pure_python | 226 us                                                                 | 275 us: 1.22x slower                                          |
| pickle_pure_python   | 322 us                                                                 | 399 us: 1.24x slower                                          |
| xml_etree_process    | 60.6 ms                                                                | 75.6 ms: 1.25x slower                                         |
| tomli_loads          | 1.96 sec                                                               | 2.49 sec: 1.27x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.15x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.3 ms: 1.04x slower                                         |
| python_startup_no_site | 7.43 ms                                                                | 9.53 ms: 1.28x slower                                         |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| django_template | 36.4 ms                                                                | 45.0 ms: 1.24x slower                                         |
| genshi_xml      | 49.9 ms                                                                | 64.0 ms: 1.28x slower                                         |
| genshi_text     | 21.7 ms                                                                | 29.9 ms: 1.38x slower                                         |
| mako            | 11.8 ms                                                                | 16.3 ms: 1.38x slower                                         |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| create_gc_cycles           | 1.82 ms                                                                | 1.32 ms: 1.38x faster                                         |
| gc_traversal               | 4.18 ms                                                                | 3.25 ms: 1.29x faster                                         |
| sqlite_synth               | 2.21 us                                                                | 2.05 us: 1.08x faster                                         |
| async_tree_io_tg           | 618 ms                                                                 | 582 ms: 1.06x faster                                          |
| async_tree_none_tg         | 260 ms                                                                 | 246 ms: 1.05x faster                                          |
| xml_etree_iterparse        | 91.5 ms                                                                | 87.9 ms: 1.04x faster                                         |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                          |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                          |
| regex_v8                   | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                         |
| pidigits                   | 192 ms                                                                 | 196 ms: 1.02x slower                                          |
| async_tree_memoization_tg  | 306 ms                                                                 | 318 ms: 1.04x slower                                          |
| async_tree_cpu_io_mixed_tg | 482 ms                                                                 | 502 ms: 1.04x slower                                          |
| python_startup             | 14.6 ms                                                                | 15.3 ms: 1.04x slower                                         |
| regex_effbot               | 2.72 ms                                                                | 2.88 ms: 1.06x slower                                         |
| regex_dna                  | 173 ms                                                                 | 183 ms: 1.06x slower                                          |
| bench_mp_pool              | 89.0 ms                                                                | 95.4 ms: 1.07x slower                                         |
| json                       | 4.98 ms                                                                | 5.34 ms: 1.07x slower                                         |
| async_tree_none            | 267 ms                                                                 | 289 ms: 1.08x slower                                          |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 537 ms: 1.09x slower                                          |
| dulwich_log                | 77.0 ms                                                                | 83.8 ms: 1.09x slower                                         |
| pycparser                  | 1.14 sec                                                               | 1.24 sec: 1.09x slower                                        |
| docutils                   | 2.60 sec                                                               | 2.86 sec: 1.10x slower                                        |
| float                      | 70.9 ms                                                                | 78.0 ms: 1.10x slower                                         |
| async_tree_memoization     | 324 ms                                                                 | 357 ms: 1.10x slower                                          |
| json_loads                 | 27.6 us                                                                | 30.6 us: 1.11x slower                                         |
| bpe_tokeniser              | 4.25 sec                                                               | 4.82 sec: 1.13x slower                                        |
| json_dumps                 | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                         |
| pylint                     | 282 ms                                                                 | 321 ms: 1.14x slower                                          |
| k_core                     | 2.05 sec                                                               | 2.33 sec: 1.14x slower                                        |
| sphinx                     | 993 ms                                                                 | 1.14 sec: 1.15x slower                                        |
| coroutines                 | 22.0 ms                                                                | 25.4 ms: 1.16x slower                                         |
| many_optionals             | 1.05 ms                                                                | 1.22 ms: 1.16x slower                                         |
| async_generators           | 322 ms                                                                 | 376 ms: 1.17x slower                                          |
| logging_silent             | 103 ns                                                                 | 121 ns: 1.17x slower                                          |
| subparsers                 | 22.4 ms                                                                | 26.4 ms: 1.18x slower                                         |
| sqlglot_normalize          | 105 ms                                                                 | 124 ms: 1.18x slower                                          |
| sqlglot_optimize           | 52.9 ms                                                                | 62.5 ms: 1.18x slower                                         |
| mdp                        | 2.31 sec                                                               | 2.74 sec: 1.19x slower                                        |
| xml_etree_generate         | 83.3 ms                                                                | 99.0 ms: 1.19x slower                                         |
| logging_simple             | 6.50 us                                                                | 7.80 us: 1.20x slower                                         |
| telco                      | 7.20 ms                                                                | 8.66 ms: 1.20x slower                                         |
| spectral_norm              | 94.0 ms                                                                | 113 ms: 1.20x slower                                          |
| sympy_expand               | 463 ms                                                                 | 561 ms: 1.21x slower                                          |
| generators                 | 27.3 ms                                                                | 33.3 ms: 1.22x slower                                         |
| unpickle_pure_python       | 226 us                                                                 | 275 us: 1.22x slower                                          |
| pprint_safe_repr           | 704 ms                                                                 | 859 ms: 1.22x slower                                          |
| logging_format             | 7.21 us                                                                | 8.81 us: 1.22x slower                                         |
| 2to3                       | 256 ms                                                                 | 314 ms: 1.22x slower                                          |
| go                         | 118 ms                                                                 | 145 ms: 1.23x slower                                          |
| sympy_sum                  | 156 ms                                                                 | 191 ms: 1.23x slower                                          |
| coverage                   | 80.0 ms                                                                | 98.8 ms: 1.23x slower                                         |
| thrift                     | 749 us                                                                 | 925 us: 1.24x slower                                          |
| django_template            | 36.4 ms                                                                | 45.0 ms: 1.24x slower                                         |
| regex_compile              | 129 ms                                                                 | 160 ms: 1.24x slower                                          |
| pickle_pure_python         | 322 us                                                                 | 399 us: 1.24x slower                                          |
| pprint_pformat             | 1.43 sec                                                               | 1.78 sec: 1.24x slower                                        |
| scimark_sor                | 113 ms                                                                 | 141 ms: 1.24x slower                                          |
| sqlalchemy_declarative     | 130 ms                                                                 | 162 ms: 1.24x slower                                          |
| sympy_integrate            | 20.0 ms                                                                | 24.9 ms: 1.24x slower                                         |
| xml_etree_process          | 60.6 ms                                                                | 75.6 ms: 1.25x slower                                         |
| sqlalchemy_imperative      | 19.8 ms                                                                | 24.7 ms: 1.25x slower                                         |
| sympy_str                  | 275 ms                                                                 | 346 ms: 1.26x slower                                          |
| deepcopy                   | 259 us                                                                 | 328 us: 1.27x slower                                          |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.27x slower                                          |
| tomli_loads                | 1.96 sec                                                               | 2.49 sec: 1.27x slower                                        |
| raytrace                   | 266 ms                                                                 | 340 ms: 1.28x slower                                          |
| scimark_fft                | 312 ms                                                                 | 398 ms: 1.28x slower                                          |
| sqlglot_transpile          | 1.56 ms                                                                | 2.00 ms: 1.28x slower                                         |
| pyflate                    | 411 ms                                                                 | 525 ms: 1.28x slower                                          |
| sqlglot_parse              | 1.25 ms                                                                | 1.61 ms: 1.28x slower                                         |
| genshi_xml                 | 49.9 ms                                                                | 64.0 ms: 1.28x slower                                         |
| python_startup_no_site     | 7.43 ms                                                                | 9.53 ms: 1.28x slower                                         |
| connected_components       | 390 ms                                                                 | 502 ms: 1.29x slower                                          |
| comprehensions             | 16.6 us                                                                | 21.3 us: 1.29x slower                                         |
| chaos                      | 56.0 ms                                                                | 72.1 ms: 1.29x slower                                         |
| shortest_path              | 427 ms                                                                 | 551 ms: 1.29x slower                                          |
| deepcopy_reduce            | 2.66 us                                                                | 3.44 us: 1.29x slower                                         |
| nqueens                    | 77.9 ms                                                                | 101 ms: 1.29x slower                                          |
| crypto_pyaes               | 67.8 ms                                                                | 88.9 ms: 1.31x slower                                         |
| hexiom                     | 5.90 ms                                                                | 7.77 ms: 1.32x slower                                         |
| typing_runtime_protocols   | 158 us                                                                 | 211 us: 1.33x slower                                          |
| deepcopy_memo              | 30.6 us                                                                | 40.8 us: 1.33x slower                                         |
| richards                   | 42.4 ms                                                                | 56.6 ms: 1.33x slower                                         |
| scimark_monte_carlo        | 63.0 ms                                                                | 84.3 ms: 1.34x slower                                         |
| fannkuch                   | 374 ms                                                                 | 502 ms: 1.34x slower                                          |
| meteor_contest             | 98.7 ms                                                                | 133 ms: 1.35x slower                                          |
| scimark_sparse_mat_mult    | 4.17 ms                                                                | 5.67 ms: 1.36x slower                                         |
| richards_super             | 48.5 ms                                                                | 66.0 ms: 1.36x slower                                         |
| genshi_text                | 21.7 ms                                                                | 29.9 ms: 1.38x slower                                         |
| mako                       | 11.8 ms                                                                | 16.3 ms: 1.38x slower                                         |
| deltablue                  | 3.20 ms                                                                | 4.77 ms: 1.49x slower                                         |
| nbody                      | 90.7 ms                                                                | 141 ms: 1.55x slower                                          |
| bench_thread_pool          | 1.04 ms                                                                | 3.32 ms: 3.21x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.19x slower                                                  |

Benchmark hidden because not significant (2): pathlib, async_tree_io
Ignored benchmarks (1) of results/bm-20250122-3.14.0a4+-fcbf62d-NOGIL/bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d.json: html5lib

- Geometric mean (including insignificant results): 1.152x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x