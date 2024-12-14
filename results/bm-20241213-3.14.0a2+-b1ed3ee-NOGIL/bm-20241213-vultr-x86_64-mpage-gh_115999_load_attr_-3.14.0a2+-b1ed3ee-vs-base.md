# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.127x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 366 ms                                                                 | 323 ms: 1.13x faster                                                  |
| docutils       | 3.07 sec                                                               | 2.87 sec: 1.07x faster                                                |
| html5lib       | 96.1 ms                                                                | 80.4 ms: 1.20x faster                                                 |
| sphinx         | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 355 ms                                                                 | 266 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 445 ms                                                                 | 337 ms: 1.32x faster                                                  |
| async_tree_io_tg           | 816 ms                                                                 | 618 ms: 1.32x faster                                                  |
| async_tree_io              | 843 ms                                                                 | 653 ms: 1.29x faster                                                  |
| async_tree_none            | 386 ms                                                                 | 306 ms: 1.26x faster                                                  |
| async_tree_memoization     | 473 ms                                                                 | 375 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg | 617 ms                                                                 | 512 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 640 ms                                                                 | 544 ms: 1.18x faster                                                  |
| async_generators           | 453 ms                                                                 | 415 ms: 1.09x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 521 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.20x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 134 ms                                                                 | 103 ms: 1.31x faster                                                  |
| nbody          | 128 ms                                                                 | 130 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 157 ms: 1.13x faster                                                  |
| regex_v8       | 25.1 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| regex_dna      | 184 ms                                                                 | 176 ms: 1.05x faster                                                  |
| regex_effbot   | 2.87 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 512 us                                                                 | 370 us: 1.38x faster                                                  |
| unpickle_pure_python | 335 us                                                                 | 254 us: 1.32x faster                                                  |
| json_dumps           | 14.2 ms                                                                | 13.2 ms: 1.08x faster                                                 |
| xml_etree_process    | 77.0 ms                                                                | 71.6 ms: 1.08x faster                                                 |
| json_loads           | 29.0 us                                                                | 28.1 us: 1.03x faster                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 87.7 ms: 1.03x faster                                                 |
| tomli_loads          | 2.56 sec                                                               | 2.52 sec: 1.01x faster                                                |
| xml_etree_generate   | 96.8 ms                                                                | 95.5 ms: 1.01x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.3 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.2 ms                                                                | 10.2 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 50.4 ms                                                                | 44.0 ms: 1.14x faster                                                 |
| genshi_text     | 31.4 ms                                                                | 27.7 ms: 1.14x faster                                                 |
| mako            | 17.5 ms                                                                | 15.6 ms: 1.13x faster                                                 |
| genshi_xml      | 63.5 ms                                                                | 60.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 269 ms                                                                 | 165 ms: 1.63x faster                                                  |
| logging_silent             | 183 ns                                                                 | 114 ns: 1.60x faster                                                  |
| deltablue                  | 8.17 ms                                                                | 5.36 ms: 1.53x faster                                                 |
| raytrace                   | 549 ms                                                                 | 372 ms: 1.48x faster                                                  |
| sqlglot_parse              | 2.59 ms                                                                | 1.85 ms: 1.40x faster                                                 |
| pickle_pure_python         | 512 us                                                                 | 370 us: 1.38x faster                                                  |
| sqlglot_transpile          | 2.96 ms                                                                | 2.18 ms: 1.36x faster                                                 |
| async_tree_none_tg         | 355 ms                                                                 | 266 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 445 ms                                                                 | 337 ms: 1.32x faster                                                  |
| async_tree_io_tg           | 816 ms                                                                 | 618 ms: 1.32x faster                                                  |
| unpickle_pure_python       | 335 us                                                                 | 254 us: 1.32x faster                                                  |
| logging_simple             | 10.7 us                                                                | 8.14 us: 1.32x faster                                                 |
| chaos                      | 104 ms                                                                 | 79.1 ms: 1.31x faster                                                 |
| pyflate                    | 680 ms                                                                 | 519 ms: 1.31x faster                                                  |
| float                      | 134 ms                                                                 | 103 ms: 1.31x faster                                                  |
| scimark_sor                | 232 ms                                                                 | 178 ms: 1.31x faster                                                  |
| async_tree_io              | 843 ms                                                                 | 653 ms: 1.29x faster                                                  |
| generators                 | 39.5 ms                                                                | 30.7 ms: 1.29x faster                                                 |
| logging_format             | 11.8 us                                                                | 9.20 us: 1.28x faster                                                 |
| comprehensions             | 27.0 us                                                                | 21.2 us: 1.28x faster                                                 |
| hexiom                     | 9.77 ms                                                                | 7.73 ms: 1.26x faster                                                 |
| async_tree_none            | 386 ms                                                                 | 306 ms: 1.26x faster                                                  |
| async_tree_memoization     | 473 ms                                                                 | 375 ms: 1.26x faster                                                  |
| scimark_monte_carlo        | 118 ms                                                                 | 94.6 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 617 ms                                                                 | 512 ms: 1.21x faster                                                  |
| html5lib                   | 96.1 ms                                                                | 80.4 ms: 1.20x faster                                                 |
| richards                   | 77.4 ms                                                                | 64.9 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 640 ms                                                                 | 544 ms: 1.18x faster                                                  |
| sqlalchemy_imperative      | 29.4 ms                                                                | 25.0 ms: 1.17x faster                                                 |
| thrift                     | 1.19 ms                                                                | 1.02 ms: 1.17x faster                                                 |
| subparsers                 | 31.5 ms                                                                | 27.3 ms: 1.15x faster                                                 |
| richards_super             | 86.1 ms                                                                | 74.8 ms: 1.15x faster                                                 |
| pprint_pformat             | 2.00 sec                                                               | 1.75 sec: 1.15x faster                                                |
| django_template            | 50.4 ms                                                                | 44.0 ms: 1.14x faster                                                 |
| pycparser                  | 1.54 sec                                                               | 1.35 sec: 1.14x faster                                                |
| pprint_safe_repr           | 963 ms                                                                 | 844 ms: 1.14x faster                                                  |
| genshi_text                | 31.4 ms                                                                | 27.7 ms: 1.14x faster                                                 |
| 2to3                       | 366 ms                                                                 | 323 ms: 1.13x faster                                                  |
| regex_compile              | 177 ms                                                                 | 157 ms: 1.13x faster                                                  |
| mako                       | 17.5 ms                                                                | 15.6 ms: 1.13x faster                                                 |
| sqlglot_normalize          | 134 ms                                                                 | 119 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 203 ms                                                                 | 181 ms: 1.12x faster                                                  |
| scimark_lu                 | 182 ms                                                                 | 163 ms: 1.11x faster                                                  |
| sqlglot_optimize           | 68.0 ms                                                                | 61.0 ms: 1.11x faster                                                 |
| dulwich_log                | 94.9 ms                                                                | 85.2 ms: 1.11x faster                                                 |
| async_generators           | 453 ms                                                                 | 415 ms: 1.09x faster                                                  |
| pylint                     | 382 ms                                                                 | 349 ms: 1.09x faster                                                  |
| many_optionals             | 1.30 ms                                                                | 1.19 ms: 1.09x faster                                                 |
| regex_v8                   | 25.1 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| json_dumps                 | 14.2 ms                                                                | 13.2 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.51 us                                                                | 3.25 us: 1.08x faster                                                 |
| mdp                        | 2.93 sec                                                               | 2.72 sec: 1.08x faster                                                |
| xml_etree_process          | 77.0 ms                                                                | 71.6 ms: 1.08x faster                                                 |
| docutils                   | 3.07 sec                                                               | 2.87 sec: 1.07x faster                                                |
| sphinx                     | 1.18 sec                                                               | 1.12 sec: 1.05x faster                                                |
| crypto_pyaes               | 91.3 ms                                                                | 86.7 ms: 1.05x faster                                                 |
| deepcopy                   | 323 us                                                                 | 307 us: 1.05x faster                                                  |
| regex_dna                  | 184 ms                                                                 | 176 ms: 1.05x faster                                                  |
| deepcopy_memo              | 39.7 us                                                                | 38.0 us: 1.05x faster                                                 |
| sqlite_synth               | 2.26 us                                                                | 2.16 us: 1.04x faster                                                 |
| pathlib                    | 20.3 ms                                                                | 19.4 ms: 1.04x faster                                                 |
| genshi_xml                 | 63.5 ms                                                                | 60.8 ms: 1.04x faster                                                 |
| sympy_str                  | 478 ms                                                                 | 458 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 4.97 sec                                                               | 4.78 sec: 1.04x faster                                                |
| regex_effbot               | 2.87 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| json_loads                 | 29.0 us                                                                | 28.1 us: 1.03x faster                                                 |
| gc_traversal               | 3.26 ms                                                                | 3.16 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 87.7 ms: 1.03x faster                                                 |
| sympy_integrate            | 29.4 ms                                                                | 28.6 ms: 1.03x faster                                                 |
| sympy_expand               | 955 ms                                                                 | 928 ms: 1.03x faster                                                  |
| scimark_fft                | 383 ms                                                                 | 373 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 203 us                                                                 | 197 us: 1.03x faster                                                  |
| sympy_sum                  | 349 ms                                                                 | 340 ms: 1.03x faster                                                  |
| json                       | 5.07 ms                                                                | 4.95 ms: 1.03x faster                                                 |
| telco                      | 8.73 ms                                                                | 8.52 ms: 1.02x faster                                                 |
| bench_thread_pool          | 3.42 ms                                                                | 3.34 ms: 1.02x faster                                                 |
| coverage                   | 101 ms                                                                 | 98.4 ms: 1.02x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| meteor_contest             | 131 ms                                                                 | 129 ms: 1.02x faster                                                  |
| k_core                     | 2.36 sec                                                               | 2.32 sec: 1.02x faster                                                |
| tomli_loads                | 2.56 sec                                                               | 2.52 sec: 1.01x faster                                                |
| python_startup             | 17.3 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| xml_etree_generate         | 96.8 ms                                                                | 95.5 ms: 1.01x faster                                                 |
| shortest_path              | 551 ms                                                                 | 546 ms: 1.01x faster                                                  |
| connected_components       | 496 ms                                                                 | 492 ms: 1.01x faster                                                  |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| fannkuch                   | 493 ms                                                                 | 490 ms: 1.01x faster                                                  |
| python_startup_no_site     | 10.2 ms                                                                | 10.2 ms: 1.00x slower                                                 |
| asyncio_websockets         | 518 ms                                                                 | 521 ms: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                                 | 110 ms: 1.01x slower                                                  |
| nbody                      | 128 ms                                                                 | 130 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 5.44 ms                                                                | 5.68 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (4): coroutines, pidigits, nqueens, create_gc_cycles

- Geometric mean (including insignificant results): 1.127x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.01x