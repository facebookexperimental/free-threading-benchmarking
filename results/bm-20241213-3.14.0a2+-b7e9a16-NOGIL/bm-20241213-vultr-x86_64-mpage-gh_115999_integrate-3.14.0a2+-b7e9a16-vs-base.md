# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.170x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 316 ms: 1.15x faster                                                 |
| docutils       | 3.08 sec                                                               | 2.83 sec: 1.09x faster                                               |
| html5lib       | 97.9 ms                                                                | 73.8 ms: 1.33x faster                                                |
| sphinx         | 1.18 sec                                                               | 1.11 sec: 1.06x faster                                               |
| Geometric mean | (ref)                                                                  | 1.15x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 347 ms                                                                 | 238 ms: 1.46x faster                                                 |
| async_tree_memoization_tg  | 433 ms                                                                 | 311 ms: 1.39x faster                                                 |
| async_tree_io              | 813 ms                                                                 | 600 ms: 1.35x faster                                                 |
| async_tree_io_tg           | 795 ms                                                                 | 588 ms: 1.35x faster                                                 |
| async_tree_none            | 375 ms                                                                 | 282 ms: 1.33x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 486 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 519 ms: 1.20x faster                                                 |
| coroutines                 | 25.0 ms                                                                | 22.6 ms: 1.11x faster                                                |
| async_generators           | 456 ms                                                                 | 413 ms: 1.10x faster                                                 |
| asyncio_websockets         | 521 ms                                                                 | 518 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 79.1 ms: 1.71x faster                                                |
| nbody          | 135 ms                                                                 | 129 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.22x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 148 ms: 1.20x faster                                                 |
| regex_dna      | 178 ms                                                                 | 172 ms: 1.03x faster                                                 |
| regex_v8       | 23.7 ms                                                                | 23.9 ms: 1.01x slower                                                |
| regex_effbot   | 2.77 ms                                                                | 2.84 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 339 us                                                                 | 239 us: 1.42x faster                                                 |
| pickle_pure_python   | 507 us                                                                 | 357 us: 1.42x faster                                                 |
| xml_etree_process    | 79.2 ms                                                                | 67.5 ms: 1.17x faster                                                |
| tomli_loads          | 2.58 sec                                                               | 2.33 sec: 1.10x faster                                               |
| json_dumps           | 14.1 ms                                                                | 13.1 ms: 1.08x faster                                                |
| xml_etree_generate   | 98.4 ms                                                                | 95.3 ms: 1.03x faster                                                |
| xml_etree_iterparse  | 89.9 ms                                                                | 88.1 ms: 1.02x faster                                                |
| json_loads           | 28.6 us                                                                | 28.2 us: 1.01x faster                                                |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.13x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                                |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 43.3 ms: 1.14x faster                                                |
| mako            | 17.1 ms                                                                | 15.4 ms: 1.11x faster                                                |
| genshi_text     | 30.4 ms                                                                | 27.7 ms: 1.10x faster                                                |
| genshi_xml      | 62.9 ms                                                                | 59.7 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| go                         | 267 ms                                                                 | 134 ms: 1.98x faster                                                 |
| deltablue                  | 8.16 ms                                                                | 4.62 ms: 1.77x faster                                                |
| raytrace                   | 548 ms                                                                 | 315 ms: 1.74x faster                                                 |
| float                      | 136 ms                                                                 | 79.1 ms: 1.71x faster                                                |
| sqlglot_parse              | 2.58 ms                                                                | 1.58 ms: 1.63x faster                                                |
| logging_silent             | 187 ns                                                                 | 118 ns: 1.59x faster                                                 |
| scimark_sor                | 233 ms                                                                 | 148 ms: 1.58x faster                                                 |
| sqlglot_transpile          | 2.96 ms                                                                | 1.91 ms: 1.55x faster                                                |
| chaos                      | 104 ms                                                                 | 69.0 ms: 1.51x faster                                                |
| scimark_monte_carlo        | 117 ms                                                                 | 80.0 ms: 1.46x faster                                                |
| async_tree_none_tg         | 347 ms                                                                 | 238 ms: 1.46x faster                                                 |
| unpickle_pure_python       | 339 us                                                                 | 239 us: 1.42x faster                                                 |
| pickle_pure_python         | 507 us                                                                 | 357 us: 1.42x faster                                                 |
| pyflate                    | 682 ms                                                                 | 481 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 433 ms                                                                 | 311 ms: 1.39x faster                                                 |
| richards                   | 77.4 ms                                                                | 55.7 ms: 1.39x faster                                                |
| logging_simple             | 10.0 us                                                                | 7.30 us: 1.37x faster                                                |
| comprehensions             | 27.9 us                                                                | 20.4 us: 1.37x faster                                                |
| async_tree_io              | 813 ms                                                                 | 600 ms: 1.35x faster                                                 |
| async_tree_io_tg           | 795 ms                                                                 | 588 ms: 1.35x faster                                                 |
| hexiom                     | 9.90 ms                                                                | 7.41 ms: 1.34x faster                                                |
| richards_super             | 86.0 ms                                                                | 64.5 ms: 1.33x faster                                                |
| logging_format             | 11.2 us                                                                | 8.38 us: 1.33x faster                                                |
| async_tree_none            | 375 ms                                                                 | 282 ms: 1.33x faster                                                 |
| html5lib                   | 97.9 ms                                                                | 73.8 ms: 1.33x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                 |
| generators                 | 38.8 ms                                                                | 30.5 ms: 1.27x faster                                                |
| pycparser                  | 1.52 sec                                                               | 1.22 sec: 1.25x faster                                               |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 486 ms: 1.24x faster                                                 |
| thrift                     | 1.09 ms                                                                | 906 us: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 519 ms: 1.20x faster                                                 |
| subparsers                 | 30.8 ms                                                                | 25.6 ms: 1.20x faster                                                |
| regex_compile              | 177 ms                                                                 | 148 ms: 1.20x faster                                                 |
| sqlalchemy_imperative      | 28.8 ms                                                                | 24.3 ms: 1.18x faster                                                |
| xml_etree_process          | 79.2 ms                                                                | 67.5 ms: 1.17x faster                                                |
| dulwich_log                | 94.4 ms                                                                | 81.0 ms: 1.16x faster                                                |
| pprint_pformat             | 2.02 sec                                                               | 1.74 sec: 1.16x faster                                               |
| pprint_safe_repr           | 974 ms                                                                 | 844 ms: 1.16x faster                                                 |
| 2to3                       | 365 ms                                                                 | 316 ms: 1.15x faster                                                 |
| django_template            | 49.5 ms                                                                | 43.3 ms: 1.14x faster                                                |
| sqlalchemy_declarative     | 201 ms                                                                 | 176 ms: 1.14x faster                                                 |
| mdp                        | 2.89 sec                                                               | 2.58 sec: 1.12x faster                                               |
| sqlglot_normalize          | 134 ms                                                                 | 120 ms: 1.11x faster                                                 |
| mako                       | 17.1 ms                                                                | 15.4 ms: 1.11x faster                                                |
| coroutines                 | 25.0 ms                                                                | 22.6 ms: 1.11x faster                                                |
| tomli_loads                | 2.58 sec                                                               | 2.33 sec: 1.10x faster                                               |
| async_generators           | 456 ms                                                                 | 413 ms: 1.10x faster                                                 |
| scimark_lu                 | 184 ms                                                                 | 167 ms: 1.10x faster                                                 |
| genshi_text                | 30.4 ms                                                                | 27.7 ms: 1.10x faster                                                |
| docutils                   | 3.08 sec                                                               | 2.83 sec: 1.09x faster                                               |
| pylint                     | 371 ms                                                                 | 341 ms: 1.09x faster                                                 |
| sqlglot_optimize           | 66.2 ms                                                                | 61.0 ms: 1.09x faster                                                |
| deepcopy_reduce            | 3.49 us                                                                | 3.24 us: 1.08x faster                                                |
| json_dumps                 | 14.1 ms                                                                | 13.1 ms: 1.08x faster                                                |
| many_optionals             | 1.25 ms                                                                | 1.16 ms: 1.07x faster                                                |
| sqlite_synth               | 2.18 us                                                                | 2.05 us: 1.06x faster                                                |
| bpe_tokeniser              | 5.03 sec                                                               | 4.74 sec: 1.06x faster                                               |
| deepcopy_memo              | 40.6 us                                                                | 38.4 us: 1.06x faster                                                |
| sphinx                     | 1.18 sec                                                               | 1.11 sec: 1.06x faster                                               |
| genshi_xml                 | 62.9 ms                                                                | 59.7 ms: 1.05x faster                                                |
| sympy_str                  | 479 ms                                                                 | 455 ms: 1.05x faster                                                 |
| pathlib                    | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                |
| coverage                   | 104 ms                                                                 | 99.3 ms: 1.05x faster                                                |
| nbody                      | 135 ms                                                                 | 129 ms: 1.05x faster                                                 |
| crypto_pyaes               | 90.5 ms                                                                | 86.4 ms: 1.05x faster                                                |
| sympy_integrate            | 29.6 ms                                                                | 28.3 ms: 1.04x faster                                                |
| scimark_sparse_mat_mult    | 5.60 ms                                                                | 5.38 ms: 1.04x faster                                                |
| deepcopy                   | 321 us                                                                 | 309 us: 1.04x faster                                                 |
| sympy_expand               | 960 ms                                                                 | 924 ms: 1.04x faster                                                 |
| spectral_norm              | 114 ms                                                                 | 109 ms: 1.04x faster                                                 |
| fannkuch                   | 497 ms                                                                 | 479 ms: 1.04x faster                                                 |
| telco                      | 8.81 ms                                                                | 8.51 ms: 1.04x faster                                                |
| regex_dna                  | 178 ms                                                                 | 172 ms: 1.03x faster                                                 |
| xml_etree_generate         | 98.4 ms                                                                | 95.3 ms: 1.03x faster                                                |
| sympy_sum                  | 350 ms                                                                 | 339 ms: 1.03x faster                                                 |
| connected_components       | 501 ms                                                                 | 486 ms: 1.03x faster                                                 |
| json                       | 5.08 ms                                                                | 4.94 ms: 1.03x faster                                                |
| scimark_fft                | 379 ms                                                                 | 369 ms: 1.03x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 105 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 203 us                                                                 | 198 us: 1.03x faster                                                 |
| xml_etree_iterparse        | 89.9 ms                                                                | 88.1 ms: 1.02x faster                                                |
| k_core                     | 2.35 sec                                                               | 2.31 sec: 1.02x faster                                               |
| bench_thread_pool          | 3.38 ms                                                                | 3.32 ms: 1.02x faster                                                |
| shortest_path              | 555 ms                                                                 | 546 ms: 1.02x faster                                                 |
| json_loads                 | 28.6 us                                                                | 28.2 us: 1.01x faster                                                |
| nqueens                    | 96.8 ms                                                                | 95.7 ms: 1.01x faster                                                |
| python_startup             | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                                |
| create_gc_cycles           | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                                |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                |
| gc_traversal               | 3.54 ms                                                                | 3.52 ms: 1.01x faster                                                |
| asyncio_websockets         | 521 ms                                                                 | 518 ms: 1.01x faster                                                 |
| regex_v8                   | 23.7 ms                                                                | 23.9 ms: 1.01x slower                                                |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                 |
| regex_effbot               | 2.77 ms                                                                | 2.84 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.17x faster                                                         |

Benchmark hidden because not significant (2): meteor_contest, pidigits

- Geometric mean (including insignificant results): 1.170x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.02x