# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.148x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                 | 531 ms: 1.20x slower                                                 |
| docutils       | 3.71 sec                                                               | 4.14 sec: 1.12x slower                                               |
| html5lib       | 79.2 ms                                                                | 101 ms: 1.28x slower                                                 |
| sphinx         | 1.40 sec                                                               | 1.63 sec: 1.16x slower                                               |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 370 ms                                                                 | 315 ms: 1.18x faster                                                 |
| async_tree_io_tg           | 893 ms                                                                 | 764 ms: 1.17x faster                                                 |
| async_tree_io              | 884 ms                                                                 | 828 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 637 ms: 1.06x faster                                                 |
| asyncio_websockets         | 749 ms                                                                 | 730 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 686 ms                                                                 | 718 ms: 1.05x slower                                                 |
| async_tree_none            | 376 ms                                                                 | 406 ms: 1.08x slower                                                 |
| coroutines                 | 29.4 ms                                                                | 31.9 ms: 1.09x slower                                                |
| async_tree_memoization     | 494 ms                                                                 | 536 ms: 1.09x slower                                                 |
| async_generators           | 547 ms                                                                 | 600 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 123 ms                                                                 | 174 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.46 ms                                                                | 4.15 ms: 1.07x faster                                                |
| regex_dna      | 264 ms                                                                 | 279 ms: 1.06x slower                                                 |
| regex_compile  | 164 ms                                                                 | 209 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 199 ms                                                                 | 209 ms: 1.05x slower                                                 |
| json_loads           | 33.8 us                                                                | 36.6 us: 1.08x slower                                                |
| json_dumps           | 15.4 ms                                                                | 16.9 ms: 1.10x slower                                                |
| xml_etree_generate   | 117 ms                                                                 | 132 ms: 1.13x slower                                                 |
| unpickle_pure_python | 286 us                                                                 | 328 us: 1.15x slower                                                 |
| pickle_pure_python   | 416 us                                                                 | 486 us: 1.17x slower                                                 |
| tomli_loads          | 2.55 sec                                                               | 3.02 sec: 1.18x slower                                               |
| xml_etree_process    | 82.3 ms                                                                | 97.6 ms: 1.19x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 26.4 ms                                                                | 31.4 ms: 1.19x slower                                                |
| python_startup_no_site | 14.6 ms                                                                | 19.9 ms: 1.36x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 46.6 ms                                                                | 51.7 ms: 1.11x slower                                                |
| genshi_xml      | 68.5 ms                                                                | 81.5 ms: 1.19x slower                                                |
| genshi_text     | 28.1 ms                                                                | 36.3 ms: 1.29x slower                                                |
| mako            | 16.1 ms                                                                | 23.7 ms: 1.47x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.26x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 370 ms                                                                 | 315 ms: 1.18x faster                                                 |
| async_tree_io_tg           | 893 ms                                                                 | 764 ms: 1.17x faster                                                 |
| gc_traversal               | 7.36 ms                                                                | 6.76 ms: 1.09x faster                                                |
| regex_effbot               | 4.46 ms                                                                | 4.15 ms: 1.07x faster                                                |
| async_tree_io              | 884 ms                                                                 | 828 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 637 ms: 1.06x faster                                                 |
| asyncio_websockets         | 749 ms                                                                 | 730 ms: 1.03x faster                                                 |
| json                       | 6.52 ms                                                                | 6.80 ms: 1.04x slower                                                |
| sqlite_synth               | 3.55 us                                                                | 3.71 us: 1.04x slower                                                |
| async_tree_cpu_io_mixed    | 686 ms                                                                 | 718 ms: 1.05x slower                                                 |
| xml_etree_parse            | 199 ms                                                                 | 209 ms: 1.05x slower                                                 |
| regex_dna                  | 264 ms                                                                 | 279 ms: 1.06x slower                                                 |
| logging_silent             | 141 ns                                                                 | 149 ns: 1.06x slower                                                 |
| generators                 | 40.0 ms                                                                | 42.5 ms: 1.06x slower                                                |
| k_core                     | 4.00 sec                                                               | 4.27 sec: 1.07x slower                                               |
| async_tree_none            | 376 ms                                                                 | 406 ms: 1.08x slower                                                 |
| json_loads                 | 33.8 us                                                                | 36.6 us: 1.08x slower                                                |
| coroutines                 | 29.4 ms                                                                | 31.9 ms: 1.09x slower                                                |
| async_tree_memoization     | 494 ms                                                                 | 536 ms: 1.09x slower                                                 |
| async_generators           | 547 ms                                                                 | 600 ms: 1.10x slower                                                 |
| json_dumps                 | 15.4 ms                                                                | 16.9 ms: 1.10x slower                                                |
| django_template            | 46.6 ms                                                                | 51.7 ms: 1.11x slower                                                |
| mdp                        | 3.70 sec                                                               | 4.13 sec: 1.12x slower                                               |
| docutils                   | 3.71 sec                                                               | 4.14 sec: 1.12x slower                                               |
| shortest_path              | 887 ms                                                                 | 997 ms: 1.12x slower                                                 |
| connected_components       | 816 ms                                                                 | 919 ms: 1.13x slower                                                 |
| xml_etree_generate         | 117 ms                                                                 | 132 ms: 1.13x slower                                                 |
| logging_simple             | 8.06 us                                                                | 9.14 us: 1.13x slower                                                |
| spectral_norm              | 135 ms                                                                 | 153 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 137 ms                                                                 | 156 ms: 1.13x slower                                                 |
| pycparser                  | 1.50 sec                                                               | 1.70 sec: 1.14x slower                                               |
| sqlglot_optimize           | 70.2 ms                                                                | 80.2 ms: 1.14x slower                                                |
| unpickle_pure_python       | 286 us                                                                 | 328 us: 1.15x slower                                                 |
| coverage                   | 110 ms                                                                 | 126 ms: 1.15x slower                                                 |
| pyflate                    | 637 ms                                                                 | 735 ms: 1.15x slower                                                 |
| deepcopy_reduce            | 3.67 us                                                                | 4.24 us: 1.15x slower                                                |
| sphinx                     | 1.40 sec                                                               | 1.63 sec: 1.16x slower                                               |
| dulwich_log                | 91.6 ms                                                                | 107 ms: 1.16x slower                                                 |
| scimark_sor                | 160 ms                                                                 | 186 ms: 1.17x slower                                                 |
| pickle_pure_python         | 416 us                                                                 | 486 us: 1.17x slower                                                 |
| logging_format             | 9.35 us                                                                | 11.0 us: 1.18x slower                                                |
| tomli_loads                | 2.55 sec                                                               | 3.02 sec: 1.18x slower                                               |
| xml_etree_process          | 82.3 ms                                                                | 97.6 ms: 1.19x slower                                                |
| bench_thread_pool          | 3.05 ms                                                                | 3.63 ms: 1.19x slower                                                |
| genshi_xml                 | 68.5 ms                                                                | 81.5 ms: 1.19x slower                                                |
| python_startup             | 26.4 ms                                                                | 31.4 ms: 1.19x slower                                                |
| 2to3                       | 444 ms                                                                 | 531 ms: 1.20x slower                                                 |
| pprint_pformat             | 1.93 sec                                                               | 2.31 sec: 1.20x slower                                               |
| richards                   | 59.5 ms                                                                | 71.8 ms: 1.21x slower                                                |
| pprint_safe_repr           | 935 ms                                                                 | 1.13 sec: 1.21x slower                                               |
| subparsers                 | 30.9 ms                                                                | 37.6 ms: 1.22x slower                                                |
| comprehensions             | 21.6 us                                                                | 26.4 us: 1.22x slower                                                |
| scimark_sparse_mat_mult    | 6.32 ms                                                                | 7.75 ms: 1.23x slower                                                |
| scimark_fft                | 436 ms                                                                 | 535 ms: 1.23x slower                                                 |
| go                         | 151 ms                                                                 | 185 ms: 1.23x slower                                                 |
| telco                      | 10.2 ms                                                                | 12.5 ms: 1.23x slower                                                |
| raytrace                   | 352 ms                                                                 | 435 ms: 1.24x slower                                                 |
| bpe_tokeniser              | 5.91 sec                                                               | 7.32 sec: 1.24x slower                                               |
| pylint                     | 392 ms                                                                 | 487 ms: 1.24x slower                                                 |
| sqlglot_parse              | 1.82 ms                                                                | 2.27 ms: 1.25x slower                                                |
| chaos                      | 84.2 ms                                                                | 105 ms: 1.25x slower                                                 |
| deepcopy                   | 331 us                                                                 | 415 us: 1.25x slower                                                 |
| sqlglot_transpile          | 2.11 ms                                                                | 2.66 ms: 1.26x slower                                                |
| many_optionals             | 1.08 ms                                                                | 1.38 ms: 1.27x slower                                                |
| scimark_monte_carlo        | 86.2 ms                                                                | 110 ms: 1.27x slower                                                 |
| meteor_contest             | 131 ms                                                                 | 167 ms: 1.27x slower                                                 |
| regex_compile              | 164 ms                                                                 | 209 ms: 1.28x slower                                                 |
| nqueens                    | 98.2 ms                                                                | 125 ms: 1.28x slower                                                 |
| html5lib                   | 79.2 ms                                                                | 101 ms: 1.28x slower                                                 |
| fannkuch                   | 494 ms                                                                 | 636 ms: 1.29x slower                                                 |
| genshi_text                | 28.1 ms                                                                | 36.3 ms: 1.29x slower                                                |
| hexiom                     | 7.93 ms                                                                | 10.2 ms: 1.29x slower                                                |
| crypto_pyaes               | 93.1 ms                                                                | 121 ms: 1.30x slower                                                 |
| deepcopy_memo              | 40.1 us                                                                | 52.2 us: 1.30x slower                                                |
| richards_super             | 65.6 ms                                                                | 85.5 ms: 1.30x slower                                                |
| thrift                     | 1.00 ms                                                                | 1.33 ms: 1.33x slower                                                |
| typing_runtime_protocols   | 203 us                                                                 | 273 us: 1.34x slower                                                 |
| scimark_lu                 | 149 ms                                                                 | 203 ms: 1.36x slower                                                 |
| python_startup_no_site     | 14.6 ms                                                                | 19.9 ms: 1.36x slower                                                |
| deltablue                  | 4.44 ms                                                                | 6.28 ms: 1.41x slower                                                |
| nbody                      | 123 ms                                                                 | 174 ms: 1.42x slower                                                 |
| sqlalchemy_imperative      | 23.1 ms                                                                | 32.9 ms: 1.42x slower                                                |
| sympy_integrate            | 26.6 ms                                                                | 38.0 ms: 1.43x slower                                                |
| sqlalchemy_declarative     | 167 ms                                                                 | 240 ms: 1.44x slower                                                 |
| mako                       | 16.1 ms                                                                | 23.7 ms: 1.47x slower                                                |
| sympy_str                  | 344 ms                                                                 | 565 ms: 1.64x slower                                                 |
| sympy_expand               | 618 ms                                                                 | 1.08 sec: 1.75x slower                                               |
| sympy_sum                  | 200 ms                                                                 | 395 ms: 1.98x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                         |

Benchmark hidden because not significant (8): async_tree_memoization_tg, bench_mp_pool, float, xml_etree_iterparse, regex_v8, pathlib, pidigits, create_gc_cycles

- Geometric mean (including insignificant results): 1.148x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x