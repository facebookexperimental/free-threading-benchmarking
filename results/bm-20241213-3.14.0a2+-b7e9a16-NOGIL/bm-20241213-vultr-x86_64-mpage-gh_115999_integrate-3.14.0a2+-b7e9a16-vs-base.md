# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 318 ms: 1.15x faster                                                 |
| docutils       | 3.08 sec                                                               | 2.84 sec: 1.08x faster                                               |
| html5lib       | 97.9 ms                                                                | 75.3 ms: 1.30x faster                                                |
| sphinx         | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                               |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 347 ms                                                                 | 239 ms: 1.45x faster                                                 |
| async_tree_memoization_tg  | 433 ms                                                                 | 309 ms: 1.40x faster                                                 |
| async_tree_io              | 813 ms                                                                 | 604 ms: 1.35x faster                                                 |
| async_tree_io_tg           | 795 ms                                                                 | 591 ms: 1.35x faster                                                 |
| async_tree_none            | 375 ms                                                                 | 283 ms: 1.32x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 481 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 514 ms: 1.22x faster                                                 |
| coroutines                 | 25.0 ms                                                                | 23.1 ms: 1.08x faster                                                |
| async_generators           | 456 ms                                                                 | 422 ms: 1.08x faster                                                 |
| asyncio_websockets         | 521 ms                                                                 | 519 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 83.0 ms: 1.64x faster                                                |
| nbody          | 135 ms                                                                 | 133 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.19x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 151 ms: 1.17x faster                                                 |
| regex_dna      | 178 ms                                                                 | 176 ms: 1.01x faster                                                 |
| regex_v8       | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                |
| regex_effbot   | 2.77 ms                                                                | 2.86 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 507 us                                                                 | 365 us: 1.39x faster                                                 |
| unpickle_pure_python | 339 us                                                                 | 248 us: 1.37x faster                                                 |
| xml_etree_process    | 79.2 ms                                                                | 68.6 ms: 1.15x faster                                                |
| tomli_loads          | 2.58 sec                                                               | 2.34 sec: 1.10x faster                                               |
| json_dumps           | 14.1 ms                                                                | 13.2 ms: 1.06x faster                                                |
| json_loads           | 28.6 us                                                                | 27.8 us: 1.03x faster                                                |
| xml_etree_generate   | 98.4 ms                                                                | 96.4 ms: 1.02x faster                                                |
| xml_etree_iterparse  | 89.9 ms                                                                | 88.1 ms: 1.02x faster                                                |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.12x faster                                                         |

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
| django_template | 49.5 ms                                                                | 43.4 ms: 1.14x faster                                                |
| mako            | 17.1 ms                                                                | 15.6 ms: 1.09x faster                                                |
| genshi_text     | 30.4 ms                                                                | 28.1 ms: 1.08x faster                                                |
| genshi_xml      | 62.9 ms                                                                | 59.6 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.09x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| go                         | 267 ms                                                                 | 142 ms: 1.87x faster                                                 |
| deltablue                  | 8.16 ms                                                                | 4.72 ms: 1.73x faster                                                |
| raytrace                   | 548 ms                                                                 | 331 ms: 1.65x faster                                                 |
| float                      | 136 ms                                                                 | 83.0 ms: 1.64x faster                                                |
| logging_silent             | 187 ns                                                                 | 117 ns: 1.60x faster                                                 |
| sqlglot_parse              | 2.58 ms                                                                | 1.62 ms: 1.60x faster                                                |
| scimark_sor                | 233 ms                                                                 | 149 ms: 1.57x faster                                                 |
| sqlglot_transpile          | 2.96 ms                                                                | 1.94 ms: 1.52x faster                                                |
| chaos                      | 104 ms                                                                 | 71.2 ms: 1.46x faster                                                |
| async_tree_none_tg         | 347 ms                                                                 | 239 ms: 1.45x faster                                                 |
| scimark_monte_carlo        | 117 ms                                                                 | 81.2 ms: 1.44x faster                                                |
| async_tree_memoization_tg  | 433 ms                                                                 | 309 ms: 1.40x faster                                                 |
| pickle_pure_python         | 507 us                                                                 | 365 us: 1.39x faster                                                 |
| logging_simple             | 10.0 us                                                                | 7.29 us: 1.37x faster                                                |
| pyflate                    | 682 ms                                                                 | 498 ms: 1.37x faster                                                 |
| unpickle_pure_python       | 339 us                                                                 | 248 us: 1.37x faster                                                 |
| richards                   | 77.4 ms                                                                | 56.8 ms: 1.36x faster                                                |
| logging_format             | 11.2 us                                                                | 8.27 us: 1.35x faster                                                |
| async_tree_io              | 813 ms                                                                 | 604 ms: 1.35x faster                                                 |
| async_tree_io_tg           | 795 ms                                                                 | 591 ms: 1.35x faster                                                 |
| async_tree_none            | 375 ms                                                                 | 283 ms: 1.32x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                 |
| richards_super             | 86.0 ms                                                                | 66.1 ms: 1.30x faster                                                |
| comprehensions             | 27.9 us                                                                | 21.5 us: 1.30x faster                                                |
| html5lib                   | 97.9 ms                                                                | 75.3 ms: 1.30x faster                                                |
| hexiom                     | 9.90 ms                                                                | 7.65 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 481 ms: 1.25x faster                                                 |
| pycparser                  | 1.52 sec                                                               | 1.22 sec: 1.24x faster                                               |
| generators                 | 38.8 ms                                                                | 31.6 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed    | 625 ms                                                                 | 514 ms: 1.22x faster                                                 |
| subparsers                 | 30.8 ms                                                                | 25.5 ms: 1.21x faster                                                |
| thrift                     | 1.09 ms                                                                | 915 us: 1.20x faster                                                 |
| sqlalchemy_imperative      | 28.8 ms                                                                | 24.3 ms: 1.18x faster                                                |
| regex_compile              | 177 ms                                                                 | 151 ms: 1.17x faster                                                 |
| xml_etree_process          | 79.2 ms                                                                | 68.6 ms: 1.15x faster                                                |
| pprint_pformat             | 2.02 sec                                                               | 1.76 sec: 1.15x faster                                               |
| dulwich_log                | 94.4 ms                                                                | 82.2 ms: 1.15x faster                                                |
| 2to3                       | 365 ms                                                                 | 318 ms: 1.15x faster                                                 |
| scimark_lu                 | 184 ms                                                                 | 161 ms: 1.14x faster                                                 |
| pprint_safe_repr           | 974 ms                                                                 | 854 ms: 1.14x faster                                                 |
| django_template            | 49.5 ms                                                                | 43.4 ms: 1.14x faster                                                |
| sqlalchemy_declarative     | 201 ms                                                                 | 177 ms: 1.14x faster                                                 |
| tomli_loads                | 2.58 sec                                                               | 2.34 sec: 1.10x faster                                               |
| sqlglot_normalize          | 134 ms                                                                 | 122 ms: 1.10x faster                                                 |
| mako                       | 17.1 ms                                                                | 15.6 ms: 1.09x faster                                                |
| docutils                   | 3.08 sec                                                               | 2.84 sec: 1.08x faster                                               |
| pylint                     | 371 ms                                                                 | 343 ms: 1.08x faster                                                 |
| sqlglot_optimize           | 66.2 ms                                                                | 61.2 ms: 1.08x faster                                                |
| coroutines                 | 25.0 ms                                                                | 23.1 ms: 1.08x faster                                                |
| async_generators           | 456 ms                                                                 | 422 ms: 1.08x faster                                                 |
| genshi_text                | 30.4 ms                                                                | 28.1 ms: 1.08x faster                                                |
| gc_traversal               | 3.54 ms                                                                | 3.29 ms: 1.08x faster                                                |
| sqlite_synth               | 2.18 us                                                                | 2.04 us: 1.07x faster                                                |
| deepcopy_reduce            | 3.49 us                                                                | 3.28 us: 1.06x faster                                                |
| json_dumps                 | 14.1 ms                                                                | 13.2 ms: 1.06x faster                                                |
| bpe_tokeniser              | 5.03 sec                                                               | 4.74 sec: 1.06x faster                                               |
| many_optionals             | 1.25 ms                                                                | 1.18 ms: 1.06x faster                                                |
| coverage                   | 104 ms                                                                 | 98.7 ms: 1.06x faster                                                |
| scimark_sparse_mat_mult    | 5.60 ms                                                                | 5.31 ms: 1.06x faster                                                |
| genshi_xml                 | 62.9 ms                                                                | 59.6 ms: 1.05x faster                                                |
| sphinx                     | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                               |
| spectral_norm              | 114 ms                                                                 | 108 ms: 1.05x faster                                                 |
| crypto_pyaes               | 90.5 ms                                                                | 86.4 ms: 1.05x faster                                                |
| pathlib                    | 19.7 ms                                                                | 18.9 ms: 1.05x faster                                                |
| mdp                        | 2.89 sec                                                               | 2.76 sec: 1.05x faster                                               |
| sympy_str                  | 479 ms                                                                 | 458 ms: 1.04x faster                                                 |
| deepcopy_memo              | 40.6 us                                                                | 39.0 us: 1.04x faster                                                |
| sympy_integrate            | 29.6 ms                                                                | 28.4 ms: 1.04x faster                                                |
| telco                      | 8.81 ms                                                                | 8.46 ms: 1.04x faster                                                |
| sympy_expand               | 960 ms                                                                 | 927 ms: 1.04x faster                                                 |
| fannkuch                   | 497 ms                                                                 | 480 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.80 ms: 1.03x faster                                                |
| json_loads                 | 28.6 us                                                                | 27.8 us: 1.03x faster                                                |
| json                       | 5.08 ms                                                                | 4.94 ms: 1.03x faster                                                |
| sympy_sum                  | 350 ms                                                                 | 340 ms: 1.03x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 105 ms: 1.03x faster                                                 |
| scimark_fft                | 379 ms                                                                 | 371 ms: 1.02x faster                                                 |
| xml_etree_generate         | 98.4 ms                                                                | 96.4 ms: 1.02x faster                                                |
| xml_etree_iterparse        | 89.9 ms                                                                | 88.1 ms: 1.02x faster                                                |
| connected_components       | 501 ms                                                                 | 492 ms: 1.02x faster                                                 |
| deepcopy                   | 321 us                                                                 | 315 us: 1.02x faster                                                 |
| nbody                      | 135 ms                                                                 | 133 ms: 1.02x faster                                                 |
| shortest_path              | 555 ms                                                                 | 546 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 203 us                                                                 | 200 us: 1.02x faster                                                 |
| bench_thread_pool          | 3.38 ms                                                                | 3.33 ms: 1.02x faster                                                |
| k_core                     | 2.35 sec                                                               | 2.32 sec: 1.02x faster                                               |
| python_startup             | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                                |
| regex_dna                  | 178 ms                                                                 | 176 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                |
| asyncio_websockets         | 521 ms                                                                 | 519 ms: 1.01x faster                                                 |
| nqueens                    | 96.8 ms                                                                | 96.5 ms: 1.00x faster                                                |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                 |
| meteor_contest             | 128 ms                                                                 | 130 ms: 1.01x slower                                                 |
| regex_v8                   | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                |
| regex_effbot               | 2.77 ms                                                                | 2.86 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.16x faster                                                         |

Benchmark hidden because not significant (1): pidigits

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.02x