# Results vs. base

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 316 ms: 1.16x faster                                                  |
| docutils       | 3.08 sec                                                               | 2.85 sec: 1.08x faster                                                |
| html5lib       | 97.9 ms                                                                | 75.2 ms: 1.30x faster                                                 |
| sphinx         | 1.18 sec                                                               | 1.11 sec: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 347 ms                                                                 | 238 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 433 ms                                                                 | 309 ms: 1.40x faster                                                  |
| async_tree_io_tg           | 795 ms                                                                 | 586 ms: 1.36x faster                                                  |
| async_tree_io              | 813 ms                                                                 | 600 ms: 1.35x faster                                                  |
| async_tree_none            | 375 ms                                                                 | 281 ms: 1.33x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 476 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 511 ms: 1.22x faster                                                  |
| async_generators           | 456 ms                                                                 | 411 ms: 1.11x faster                                                  |
| coroutines                 | 25.0 ms                                                                | 23.8 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 80.7 ms: 1.68x faster                                                 |
| nbody          | 135 ms                                                                 | 130 ms: 1.04x faster                                                  |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.20x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 150 ms: 1.18x faster                                                  |
| regex_v8       | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                 |
| regex_dna      | 178 ms                                                                 | 182 ms: 1.02x slower                                                  |
| regex_effbot   | 2.77 ms                                                                | 2.93 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 507 us                                                                 | 366 us: 1.39x faster                                                  |
| unpickle_pure_python | 339 us                                                                 | 250 us: 1.35x faster                                                  |
| xml_etree_process    | 79.2 ms                                                                | 67.8 ms: 1.17x faster                                                 |
| tomli_loads          | 2.58 sec                                                               | 2.33 sec: 1.10x faster                                                |
| json_dumps           | 14.1 ms                                                                | 13.2 ms: 1.07x faster                                                 |
| xml_etree_generate   | 98.4 ms                                                                | 95.6 ms: 1.03x faster                                                 |
| json_loads           | 28.6 us                                                                | 28.0 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 89.9 ms                                                                | 88.7 ms: 1.01x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 130 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 43.3 ms: 1.14x faster                                                 |
| genshi_text     | 30.4 ms                                                                | 27.0 ms: 1.12x faster                                                 |
| mako            | 17.1 ms                                                                | 15.5 ms: 1.10x faster                                                 |
| genshi_xml      | 62.9 ms                                                                | 58.7 ms: 1.07x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 267 ms                                                                 | 138 ms: 1.94x faster                                                  |
| deltablue                  | 8.16 ms                                                                | 4.61 ms: 1.77x faster                                                 |
| raytrace                   | 548 ms                                                                 | 326 ms: 1.68x faster                                                  |
| float                      | 136 ms                                                                 | 80.7 ms: 1.68x faster                                                 |
| sqlglot_parse              | 2.58 ms                                                                | 1.60 ms: 1.61x faster                                                 |
| logging_silent             | 187 ns                                                                 | 117 ns: 1.59x faster                                                  |
| scimark_sor                | 233 ms                                                                 | 151 ms: 1.55x faster                                                  |
| sqlglot_transpile          | 2.96 ms                                                                | 1.93 ms: 1.53x faster                                                 |
| chaos                      | 104 ms                                                                 | 70.3 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 347 ms                                                                 | 238 ms: 1.45x faster                                                  |
| scimark_monte_carlo        | 117 ms                                                                 | 81.5 ms: 1.44x faster                                                 |
| pyflate                    | 682 ms                                                                 | 477 ms: 1.43x faster                                                  |
| comprehensions             | 27.9 us                                                                | 19.9 us: 1.41x faster                                                 |
| async_tree_memoization_tg  | 433 ms                                                                 | 309 ms: 1.40x faster                                                  |
| pickle_pure_python         | 507 us                                                                 | 366 us: 1.39x faster                                                  |
| logging_simple             | 10.0 us                                                                | 7.27 us: 1.38x faster                                                 |
| richards                   | 77.4 ms                                                                | 56.9 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 795 ms                                                                 | 586 ms: 1.36x faster                                                  |
| async_tree_io              | 813 ms                                                                 | 600 ms: 1.35x faster                                                  |
| unpickle_pure_python       | 339 us                                                                 | 250 us: 1.35x faster                                                  |
| logging_format             | 11.2 us                                                                | 8.36 us: 1.33x faster                                                 |
| async_tree_none            | 375 ms                                                                 | 281 ms: 1.33x faster                                                  |
| hexiom                     | 9.90 ms                                                                | 7.43 ms: 1.33x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                  |
| richards_super             | 86.0 ms                                                                | 65.6 ms: 1.31x faster                                                 |
| html5lib                   | 97.9 ms                                                                | 75.2 ms: 1.30x faster                                                 |
| generators                 | 38.8 ms                                                                | 30.5 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 476 ms: 1.27x faster                                                  |
| pycparser                  | 1.52 sec                                                               | 1.23 sec: 1.24x faster                                                |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 511 ms: 1.22x faster                                                  |
| thrift                     | 1.09 ms                                                                | 920 us: 1.19x faster                                                  |
| subparsers                 | 30.8 ms                                                                | 25.9 ms: 1.19x faster                                                 |
| regex_compile              | 177 ms                                                                 | 150 ms: 1.18x faster                                                  |
| pprint_pformat             | 2.02 sec                                                               | 1.72 sec: 1.17x faster                                                |
| xml_etree_process          | 79.2 ms                                                                | 67.8 ms: 1.17x faster                                                 |
| pprint_safe_repr           | 974 ms                                                                 | 836 ms: 1.17x faster                                                  |
| sqlalchemy_imperative      | 28.8 ms                                                                | 24.7 ms: 1.17x faster                                                 |
| 2to3                       | 365 ms                                                                 | 316 ms: 1.16x faster                                                  |
| django_template            | 49.5 ms                                                                | 43.3 ms: 1.14x faster                                                 |
| dulwich_log                | 94.4 ms                                                                | 82.7 ms: 1.14x faster                                                 |
| sqlalchemy_declarative     | 201 ms                                                                 | 177 ms: 1.13x faster                                                  |
| genshi_text                | 30.4 ms                                                                | 27.0 ms: 1.12x faster                                                 |
| scimark_lu                 | 184 ms                                                                 | 164 ms: 1.12x faster                                                  |
| async_generators           | 456 ms                                                                 | 411 ms: 1.11x faster                                                  |
| sqlglot_normalize          | 134 ms                                                                 | 121 ms: 1.11x faster                                                  |
| tomli_loads                | 2.58 sec                                                               | 2.33 sec: 1.10x faster                                                |
| mako                       | 17.1 ms                                                                | 15.5 ms: 1.10x faster                                                 |
| sqlglot_optimize           | 66.2 ms                                                                | 61.0 ms: 1.09x faster                                                 |
| pylint                     | 371 ms                                                                 | 342 ms: 1.09x faster                                                  |
| docutils                   | 3.08 sec                                                               | 2.85 sec: 1.08x faster                                                |
| genshi_xml                 | 62.9 ms                                                                | 58.7 ms: 1.07x faster                                                 |
| mdp                        | 2.89 sec                                                               | 2.70 sec: 1.07x faster                                                |
| deepcopy_reduce            | 3.49 us                                                                | 3.26 us: 1.07x faster                                                 |
| json_dumps                 | 14.1 ms                                                                | 13.2 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 5.03 sec                                                               | 4.71 sec: 1.07x faster                                                |
| scimark_sparse_mat_mult    | 5.60 ms                                                                | 5.24 ms: 1.07x faster                                                 |
| deepcopy_memo              | 40.6 us                                                                | 38.4 us: 1.06x faster                                                 |
| many_optionals             | 1.25 ms                                                                | 1.18 ms: 1.06x faster                                                 |
| sqlite_synth               | 2.18 us                                                                | 2.06 us: 1.06x faster                                                 |
| coverage                   | 104 ms                                                                 | 98.6 ms: 1.06x faster                                                 |
| sphinx                     | 1.18 sec                                                               | 1.11 sec: 1.06x faster                                                |
| crypto_pyaes               | 90.5 ms                                                                | 85.9 ms: 1.05x faster                                                 |
| sympy_str                  | 479 ms                                                                 | 454 ms: 1.05x faster                                                  |
| telco                      | 8.81 ms                                                                | 8.36 ms: 1.05x faster                                                 |
| pathlib                    | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                 |
| coroutines                 | 25.0 ms                                                                | 23.8 ms: 1.05x faster                                                 |
| sympy_expand               | 960 ms                                                                 | 920 ms: 1.04x faster                                                  |
| sympy_integrate            | 29.6 ms                                                                | 28.4 ms: 1.04x faster                                                 |
| nbody                      | 135 ms                                                                 | 130 ms: 1.04x faster                                                  |
| fannkuch                   | 497 ms                                                                 | 479 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 203 us                                                                 | 196 us: 1.04x faster                                                  |
| json                       | 5.08 ms                                                                | 4.91 ms: 1.03x faster                                                 |
| nqueens                    | 96.8 ms                                                                | 93.7 ms: 1.03x faster                                                 |
| xml_etree_generate         | 98.4 ms                                                                | 95.6 ms: 1.03x faster                                                 |
| sympy_sum                  | 350 ms                                                                 | 341 ms: 1.03x faster                                                  |
| json_loads                 | 28.6 us                                                                | 28.0 us: 1.02x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| deepcopy                   | 321 us                                                                 | 314 us: 1.02x faster                                                  |
| bench_thread_pool          | 3.38 ms                                                                | 3.32 ms: 1.02x faster                                                 |
| shortest_path              | 555 ms                                                                 | 548 ms: 1.01x faster                                                  |
| k_core                     | 2.35 sec                                                               | 2.32 sec: 1.01x faster                                                |
| scimark_fft                | 379 ms                                                                 | 374 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 89.9 ms                                                                | 88.7 ms: 1.01x faster                                                 |
| connected_components       | 501 ms                                                                 | 495 ms: 1.01x faster                                                  |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.85 ms: 1.01x faster                                                 |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| xml_etree_parse            | 130 ms                                                                 | 130 ms: 1.01x slower                                                  |
| regex_v8                   | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                 |
| spectral_norm              | 114 ms                                                                 | 116 ms: 1.02x slower                                                  |
| regex_dna                  | 178 ms                                                                 | 182 ms: 1.02x slower                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.93 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.16x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, meteor_contest, gc_traversal

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.02x