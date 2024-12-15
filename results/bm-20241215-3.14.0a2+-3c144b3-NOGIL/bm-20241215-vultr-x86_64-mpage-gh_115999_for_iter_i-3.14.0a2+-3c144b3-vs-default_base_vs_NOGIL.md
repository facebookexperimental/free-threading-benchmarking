# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.151x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 316 ms: 1.23x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.85 sec: 1.12x slower                                                |
| sphinx         | 992 ms                                                                 | 1.11 sec: 1.12x slower                                                |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 256 ms                                                                 | 238 ms: 1.07x faster                                                  |
| async_tree_io              | 627 ms                                                                 | 600 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 610 ms                                                                 | 586 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 476 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 511 ms: 1.02x slower                                                  |
| async_tree_memoization     | 332 ms                                                                 | 347 ms: 1.05x slower                                                  |
| coroutines                 | 21.6 ms                                                                | 23.8 ms: 1.10x slower                                                 |
| async_generators           | 352 ms                                                                 | 411 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| float          | 76.4 ms                                                                | 80.7 ms: 1.06x slower                                                 |
| nbody          | 90.3 ms                                                                | 130 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 24.0 ms: 1.02x faster                                                 |
| regex_dna      | 175 ms                                                                 | 182 ms: 1.04x slower                                                  |
| regex_effbot   | 2.69 ms                                                                | 2.93 ms: 1.09x slower                                                 |
| regex_compile  | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 88.7 ms: 1.02x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| json_loads           | 26.1 us                                                                | 28.0 us: 1.07x slower                                                 |
| xml_etree_generate   | 84.5 ms                                                                | 95.6 ms: 1.13x slower                                                 |
| pickle_pure_python   | 323 us                                                                 | 366 us: 1.13x slower                                                  |
| xml_etree_process    | 58.8 ms                                                                | 67.8 ms: 1.15x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.2 ms: 1.17x slower                                                 |
| unpickle_pure_python | 213 us                                                                 | 250 us: 1.18x slower                                                  |
| tomli_loads          | 1.97 sec                                                               | 2.33 sec: 1.19x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.7 ms                                                                | 58.7 ms: 1.18x slower                                                 |
| django_template | 35.4 ms                                                                | 43.3 ms: 1.22x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.0 ms: 1.25x slower                                                 |
| mako            | 11.6 ms                                                                | 15.5 ms: 1.34x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                | 3.54 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 256 ms                                                                 | 238 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                                | 2.06 us: 1.07x faster                                                 |
| async_tree_io              | 627 ms                                                                 | 600 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 610 ms                                                                 | 586 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 90.6 ms                                                                | 88.7 ms: 1.02x faster                                                 |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| regex_v8                   | 24.4 ms                                                                | 24.0 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 476 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                 |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 511 ms: 1.02x slower                                                  |
| json                       | 4.76 ms                                                                | 4.91 ms: 1.03x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.04x slower                                                 |
| regex_dna                  | 175 ms                                                                 | 182 ms: 1.04x slower                                                  |
| async_tree_memoization     | 332 ms                                                                 | 347 ms: 1.05x slower                                                  |
| float                      | 76.4 ms                                                                | 80.7 ms: 1.06x slower                                                 |
| json_loads                 | 26.1 us                                                                | 28.0 us: 1.07x slower                                                 |
| dulwich_log                | 76.6 ms                                                                | 82.7 ms: 1.08x slower                                                 |
| regex_effbot               | 2.69 ms                                                                | 2.93 ms: 1.09x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.23 sec: 1.09x slower                                                |
| coroutines                 | 21.6 ms                                                                | 23.8 ms: 1.10x slower                                                 |
| logging_silent             | 106 ns                                                                 | 117 ns: 1.11x slower                                                  |
| bpe_tokeniser              | 4.24 sec                                                               | 4.71 sec: 1.11x slower                                                |
| docutils                   | 2.55 sec                                                               | 2.85 sec: 1.12x slower                                                |
| sphinx                     | 992 ms                                                                 | 1.11 sec: 1.12x slower                                                |
| generators                 | 27.1 ms                                                                | 30.5 ms: 1.12x slower                                                 |
| xml_etree_generate         | 84.5 ms                                                                | 95.6 ms: 1.13x slower                                                 |
| pickle_pure_python         | 323 us                                                                 | 366 us: 1.13x slower                                                  |
| k_core                     | 2.05 sec                                                               | 2.32 sec: 1.13x slower                                                |
| pyflate                    | 421 ms                                                                 | 477 ms: 1.13x slower                                                  |
| xml_etree_process          | 58.8 ms                                                                | 67.8 ms: 1.15x slower                                                 |
| many_optionals             | 1.02 ms                                                                | 1.18 ms: 1.15x slower                                                 |
| comprehensions             | 17.2 us                                                                | 19.9 us: 1.15x slower                                                 |
| mdp                        | 2.33 sec                                                               | 2.70 sec: 1.16x slower                                                |
| telco                      | 7.18 ms                                                                | 8.36 ms: 1.16x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.2 ms: 1.17x slower                                                 |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| nqueens                    | 80.3 ms                                                                | 93.7 ms: 1.17x slower                                                 |
| async_generators           | 352 ms                                                                 | 411 ms: 1.17x slower                                                  |
| subparsers                 | 22.2 ms                                                                | 25.9 ms: 1.17x slower                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 61.0 ms: 1.17x slower                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 121 ms: 1.17x slower                                                  |
| go                         | 117 ms                                                                 | 138 ms: 1.18x slower                                                  |
| pprint_safe_repr           | 710 ms                                                                 | 836 ms: 1.18x slower                                                  |
| regex_compile              | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| unpickle_pure_python       | 213 us                                                                 | 250 us: 1.18x slower                                                  |
| scimark_sor                | 128 ms                                                                 | 151 ms: 1.18x slower                                                  |
| genshi_xml                 | 49.7 ms                                                                | 58.7 ms: 1.18x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.27 us: 1.18x slower                                                 |
| pprint_pformat             | 1.45 sec                                                               | 1.72 sec: 1.18x slower                                                |
| tomli_loads                | 1.97 sec                                                               | 2.33 sec: 1.19x slower                                                |
| bench_mp_pool              | 88.9 ms                                                                | 106 ms: 1.19x slower                                                  |
| scimark_fft                | 314 ms                                                                 | 374 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.24 ms: 1.20x slower                                                 |
| spectral_norm              | 96.3 ms                                                                | 116 ms: 1.20x slower                                                  |
| chaos                      | 58.4 ms                                                                | 70.3 ms: 1.20x slower                                                 |
| django_template            | 35.4 ms                                                                | 43.3 ms: 1.22x slower                                                 |
| pylint                     | 280 ms                                                                 | 342 ms: 1.22x slower                                                  |
| deepcopy                   | 256 us                                                                 | 314 us: 1.22x slower                                                  |
| logging_format             | 6.79 us                                                                | 8.36 us: 1.23x slower                                                 |
| sqlglot_transpile          | 1.57 ms                                                                | 1.93 ms: 1.23x slower                                                 |
| 2to3                       | 256 ms                                                                 | 316 ms: 1.23x slower                                                  |
| coverage                   | 79.2 ms                                                                | 98.6 ms: 1.24x slower                                                 |
| connected_components       | 398 ms                                                                 | 495 ms: 1.25x slower                                                  |
| thrift                     | 738 us                                                                 | 920 us: 1.25x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 27.0 ms: 1.25x slower                                                 |
| shortest_path              | 438 ms                                                                 | 548 ms: 1.25x slower                                                  |
| raytrace                   | 260 ms                                                                 | 326 ms: 1.25x slower                                                  |
| deepcopy_reduce            | 2.60 us                                                                | 3.26 us: 1.25x slower                                                 |
| scimark_monte_carlo        | 64.7 ms                                                                | 81.5 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 155 us                                                                 | 196 us: 1.26x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                                  |
| richards                   | 44.7 ms                                                                | 56.9 ms: 1.27x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 38.4 us: 1.27x slower                                                 |
| hexiom                     | 5.84 ms                                                                | 7.43 ms: 1.27x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.28x slower                                                 |
| fannkuch                   | 372 ms                                                                 | 479 ms: 1.29x slower                                                  |
| sqlalchemy_imperative      | 19.1 ms                                                                | 24.7 ms: 1.29x slower                                                 |
| richards_super             | 50.7 ms                                                                | 65.6 ms: 1.30x slower                                                 |
| crypto_pyaes               | 65.4 ms                                                                | 85.9 ms: 1.31x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.5 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 177 ms: 1.40x slower                                                  |
| sympy_integrate            | 19.9 ms                                                                | 28.4 ms: 1.43x slower                                                 |
| nbody                      | 90.3 ms                                                                | 130 ms: 1.44x slower                                                  |
| deltablue                  | 3.17 ms                                                                | 4.61 ms: 1.45x slower                                                 |
| scimark_lu                 | 110 ms                                                                 | 164 ms: 1.50x slower                                                  |
| sympy_str                  | 271 ms                                                                 | 454 ms: 1.68x slower                                                  |
| sympy_expand               | 453 ms                                                                 | 920 ms: 2.03x slower                                                  |
| sympy_sum                  | 152 ms                                                                 | 341 ms: 2.24x slower                                                  |
| bench_thread_pool          | 1.04 ms                                                                | 3.32 ms: 3.20x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.19x slower                                                          |

Benchmark hidden because not significant (1): async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20241215-3.14.0a2+-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3.json: html5lib

- Geometric mean (including insignificant results): 1.151x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x