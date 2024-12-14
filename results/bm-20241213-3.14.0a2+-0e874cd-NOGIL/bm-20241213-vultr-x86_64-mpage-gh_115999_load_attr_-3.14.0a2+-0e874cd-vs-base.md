# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 0e874cd
- commit date: 2024-12-13
- overall geometric mean: 1.121x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 366 ms                                                                 | 323 ms: 1.13x faster                                                  |
| docutils       | 3.07 sec                                                               | 2.88 sec: 1.07x faster                                                |
| html5lib       | 96.1 ms                                                                | 80.8 ms: 1.19x faster                                                 |
| sphinx         | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 355 ms                                                                 | 271 ms: 1.31x faster                                                  |
| async_tree_memoization_tg  | 445 ms                                                                 | 346 ms: 1.29x faster                                                  |
| async_tree_io_tg           | 816 ms                                                                 | 635 ms: 1.29x faster                                                  |
| async_tree_io              | 843 ms                                                                 | 668 ms: 1.26x faster                                                  |
| async_tree_memoization     | 473 ms                                                                 | 380 ms: 1.25x faster                                                  |
| async_tree_none            | 386 ms                                                                 | 311 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 617 ms                                                                 | 515 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 640 ms                                                                 | 548 ms: 1.17x faster                                                  |
| async_generators           | 453 ms                                                                 | 421 ms: 1.08x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 521 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 134 ms                                                                 | 104 ms: 1.29x faster                                                  |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| nbody          | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 159 ms: 1.11x faster                                                  |
| regex_v8       | 25.1 ms                                                                | 23.0 ms: 1.09x faster                                                 |
| regex_dna      | 184 ms                                                                 | 177 ms: 1.04x faster                                                  |
| regex_effbot   | 2.87 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 512 us                                                                 | 372 us: 1.38x faster                                                  |
| unpickle_pure_python | 335 us                                                                 | 256 us: 1.31x faster                                                  |
| json_dumps           | 14.2 ms                                                                | 13.1 ms: 1.09x faster                                                 |
| xml_etree_process    | 77.0 ms                                                                | 71.5 ms: 1.08x faster                                                 |
| json_loads           | 29.0 us                                                                | 28.1 us: 1.03x faster                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 87.8 ms: 1.03x faster                                                 |
| xml_etree_generate   | 96.8 ms                                                                | 95.1 ms: 1.02x faster                                                 |
| tomli_loads          | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                                |
| Geometric mean       | (ref)                                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.3 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.2 ms                                                                | 10.2 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 50.4 ms                                                                | 43.6 ms: 1.16x faster                                                 |
| mako            | 17.5 ms                                                                | 15.6 ms: 1.12x faster                                                 |
| genshi_text     | 31.4 ms                                                                | 28.1 ms: 1.12x faster                                                 |
| genshi_xml      | 63.5 ms                                                                | 61.0 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 269 ms                                                                 | 167 ms: 1.61x faster                                                  |
| logging_silent             | 183 ns                                                                 | 116 ns: 1.57x faster                                                  |
| deltablue                  | 8.17 ms                                                                | 5.43 ms: 1.50x faster                                                 |
| raytrace                   | 549 ms                                                                 | 376 ms: 1.46x faster                                                  |
| sqlglot_parse              | 2.59 ms                                                                | 1.88 ms: 1.38x faster                                                 |
| pickle_pure_python         | 512 us                                                                 | 372 us: 1.38x faster                                                  |
| sqlglot_transpile          | 2.96 ms                                                                | 2.20 ms: 1.34x faster                                                 |
| logging_simple             | 10.7 us                                                                | 8.09 us: 1.32x faster                                                 |
| chaos                      | 104 ms                                                                 | 79.0 ms: 1.31x faster                                                 |
| async_tree_none_tg         | 355 ms                                                                 | 271 ms: 1.31x faster                                                  |
| unpickle_pure_python       | 335 us                                                                 | 256 us: 1.31x faster                                                  |
| logging_format             | 11.8 us                                                                | 9.10 us: 1.30x faster                                                 |
| comprehensions             | 27.0 us                                                                | 20.9 us: 1.29x faster                                                 |
| float                      | 134 ms                                                                 | 104 ms: 1.29x faster                                                  |
| async_tree_memoization_tg  | 445 ms                                                                 | 346 ms: 1.29x faster                                                  |
| async_tree_io_tg           | 816 ms                                                                 | 635 ms: 1.29x faster                                                  |
| pyflate                    | 680 ms                                                                 | 530 ms: 1.28x faster                                                  |
| scimark_sor                | 232 ms                                                                 | 181 ms: 1.28x faster                                                  |
| generators                 | 39.5 ms                                                                | 31.2 ms: 1.27x faster                                                 |
| async_tree_io              | 843 ms                                                                 | 668 ms: 1.26x faster                                                  |
| scimark_monte_carlo        | 118 ms                                                                 | 94.9 ms: 1.25x faster                                                 |
| async_tree_memoization     | 473 ms                                                                 | 380 ms: 1.25x faster                                                  |
| async_tree_none            | 386 ms                                                                 | 311 ms: 1.24x faster                                                  |
| hexiom                     | 9.77 ms                                                                | 7.90 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed_tg | 617 ms                                                                 | 515 ms: 1.20x faster                                                  |
| sqlalchemy_imperative      | 29.4 ms                                                                | 24.6 ms: 1.19x faster                                                 |
| richards                   | 77.4 ms                                                                | 65.0 ms: 1.19x faster                                                 |
| html5lib                   | 96.1 ms                                                                | 80.8 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 640 ms                                                                 | 548 ms: 1.17x faster                                                  |
| richards_super             | 86.1 ms                                                                | 74.0 ms: 1.16x faster                                                 |
| django_template            | 50.4 ms                                                                | 43.6 ms: 1.16x faster                                                 |
| subparsers                 | 31.5 ms                                                                | 27.3 ms: 1.16x faster                                                 |
| thrift                     | 1.19 ms                                                                | 1.04 ms: 1.15x faster                                                 |
| pycparser                  | 1.54 sec                                                               | 1.35 sec: 1.14x faster                                                |
| sqlalchemy_declarative     | 203 ms                                                                 | 178 ms: 1.14x faster                                                  |
| 2to3                       | 366 ms                                                                 | 323 ms: 1.13x faster                                                  |
| mako                       | 17.5 ms                                                                | 15.6 ms: 1.12x faster                                                 |
| genshi_text                | 31.4 ms                                                                | 28.1 ms: 1.12x faster                                                 |
| pprint_pformat             | 2.00 sec                                                               | 1.80 sec: 1.11x faster                                                |
| regex_compile              | 177 ms                                                                 | 159 ms: 1.11x faster                                                  |
| sqlglot_normalize          | 134 ms                                                                 | 121 ms: 1.11x faster                                                  |
| dulwich_log                | 94.9 ms                                                                | 86.0 ms: 1.10x faster                                                 |
| pprint_safe_repr           | 963 ms                                                                 | 874 ms: 1.10x faster                                                  |
| sqlglot_optimize           | 68.0 ms                                                                | 61.8 ms: 1.10x faster                                                 |
| scimark_lu                 | 182 ms                                                                 | 166 ms: 1.10x faster                                                  |
| pylint                     | 382 ms                                                                 | 349 ms: 1.09x faster                                                  |
| regex_v8                   | 25.1 ms                                                                | 23.0 ms: 1.09x faster                                                 |
| json_dumps                 | 14.2 ms                                                                | 13.1 ms: 1.09x faster                                                 |
| many_optionals             | 1.30 ms                                                                | 1.20 ms: 1.08x faster                                                 |
| xml_etree_process          | 77.0 ms                                                                | 71.5 ms: 1.08x faster                                                 |
| async_generators           | 453 ms                                                                 | 421 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.26 us                                                                | 2.11 us: 1.07x faster                                                 |
| docutils                   | 3.07 sec                                                               | 2.88 sec: 1.07x faster                                                |
| mdp                        | 2.93 sec                                                               | 2.76 sec: 1.06x faster                                                |
| crypto_pyaes               | 91.3 ms                                                                | 86.1 ms: 1.06x faster                                                 |
| sphinx                     | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                                |
| bpe_tokeniser              | 4.97 sec                                                               | 4.76 sec: 1.05x faster                                                |
| telco                      | 8.73 ms                                                                | 8.36 ms: 1.04x faster                                                 |
| regex_dna                  | 184 ms                                                                 | 177 ms: 1.04x faster                                                  |
| genshi_xml                 | 63.5 ms                                                                | 61.0 ms: 1.04x faster                                                 |
| regex_effbot               | 2.87 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| sympy_str                  | 478 ms                                                                 | 461 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.51 us                                                                | 3.39 us: 1.04x faster                                                 |
| json_loads                 | 29.0 us                                                                | 28.1 us: 1.03x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 87.8 ms: 1.03x faster                                                 |
| deepcopy_memo              | 39.7 us                                                                | 38.6 us: 1.03x faster                                                 |
| json                       | 5.07 ms                                                                | 4.93 ms: 1.03x faster                                                 |
| pathlib                    | 20.3 ms                                                                | 19.7 ms: 1.03x faster                                                 |
| deepcopy                   | 323 us                                                                 | 314 us: 1.03x faster                                                  |
| sympy_integrate            | 29.4 ms                                                                | 28.7 ms: 1.02x faster                                                 |
| gc_traversal               | 3.26 ms                                                                | 3.19 ms: 1.02x faster                                                 |
| sympy_expand               | 955 ms                                                                 | 934 ms: 1.02x faster                                                  |
| sympy_sum                  | 349 ms                                                                 | 342 ms: 1.02x faster                                                  |
| bench_thread_pool          | 3.42 ms                                                                | 3.35 ms: 1.02x faster                                                 |
| meteor_contest             | 131 ms                                                                 | 129 ms: 1.02x faster                                                  |
| bench_mp_pool              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| coverage                   | 101 ms                                                                 | 98.7 ms: 1.02x faster                                                 |
| xml_etree_generate         | 96.8 ms                                                                | 95.1 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 203 us                                                                 | 199 us: 1.02x faster                                                  |
| python_startup             | 17.3 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| tomli_loads                | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                                |
| scimark_fft                | 383 ms                                                                 | 379 ms: 1.01x faster                                                  |
| connected_components       | 496 ms                                                                 | 492 ms: 1.01x faster                                                  |
| k_core                     | 2.36 sec                                                               | 2.34 sec: 1.01x faster                                                |
| spectral_norm              | 110 ms                                                                 | 109 ms: 1.00x faster                                                  |
| fannkuch                   | 493 ms                                                                 | 492 ms: 1.00x faster                                                  |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| python_startup_no_site     | 10.2 ms                                                                | 10.2 ms: 1.00x slower                                                 |
| asyncio_websockets         | 518 ms                                                                 | 521 ms: 1.01x slower                                                  |
| nbody                      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| nqueens                    | 97.1 ms                                                                | 98.7 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 5.44 ms                                                                | 5.53 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.78 ms                                                                | 1.80 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (3): shortest_path, xml_etree_parse, coroutines

- Geometric mean (including insignificant results): 1.121x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.01x