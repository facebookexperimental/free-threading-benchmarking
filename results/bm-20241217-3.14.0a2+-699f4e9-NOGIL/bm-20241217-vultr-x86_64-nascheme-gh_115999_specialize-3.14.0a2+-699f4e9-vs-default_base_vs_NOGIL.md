# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.262x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 371 ms: 1.45x slower                                                     |
| docutils       | 2.55 sec                                                               | 3.12 sec: 1.22x slower                                                   |
| sphinx         | 992 ms                                                                 | 1.19 sec: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                     |
| coroutines                 | 21.6 ms                                                                | 25.3 ms: 1.17x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 587 ms: 1.21x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 613 ms: 1.23x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 759 ms: 1.24x slower                                                     |
| async_tree_io              | 627 ms                                                                 | 789 ms: 1.26x slower                                                     |
| async_generators           | 352 ms                                                                 | 450 ms: 1.28x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 334 ms: 1.30x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 368 ms: 1.33x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 446 ms: 1.34x slower                                                     |
| async_tree_memoization_tg  | 307 ms                                                                 | 417 ms: 1.36x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.24x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 184 ms: 1.00x faster                                                     |
| nbody          | 90.3 ms                                                                | 130 ms: 1.44x slower                                                     |
| float          | 76.4 ms                                                                | 112 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 183 ms: 1.05x slower                                                     |
| regex_effbot   | 2.69 ms                                                                | 2.92 ms: 1.09x slower                                                    |
| regex_compile  | 127 ms                                                                 | 174 ms: 1.37x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| json_loads           | 26.1 us                                                                | 28.6 us: 1.10x slower                                                    |
| xml_etree_generate   | 84.5 ms                                                                | 98.4 ms: 1.16x slower                                                    |
| xml_etree_process    | 58.8 ms                                                                | 74.3 ms: 1.26x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| tomli_loads          | 1.97 sec                                                               | 2.56 sec: 1.30x slower                                                   |
| unpickle_pure_python | 213 us                                                                 | 346 us: 1.63x slower                                                     |
| pickle_pure_python   | 323 us                                                                 | 535 us: 1.65x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.7 ms                                                                | 64.0 ms: 1.29x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 30.7 ms: 1.42x slower                                                    |
| django_template | 35.4 ms                                                                | 51.6 ms: 1.46x slower                                                    |
| mako            | 11.6 ms                                                                | 17.1 ms: 1.48x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                | 3.27 ms: 1.30x faster                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.14 us: 1.03x faster                                                    |
| create_gc_cycles           | 1.83 ms                                                                | 1.79 ms: 1.02x faster                                                    |
| pidigits                   | 185 ms                                                                 | 184 ms: 1.00x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                     |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| regex_dna                  | 175 ms                                                                 | 183 ms: 1.05x slower                                                     |
| pathlib                    | 18.2 ms                                                                | 19.4 ms: 1.07x slower                                                    |
| json                       | 4.76 ms                                                                | 5.10 ms: 1.07x slower                                                    |
| regex_effbot               | 2.69 ms                                                                | 2.92 ms: 1.09x slower                                                    |
| json_loads                 | 26.1 us                                                                | 28.6 us: 1.10x slower                                                    |
| spectral_norm              | 96.3 ms                                                                | 109 ms: 1.13x slower                                                     |
| k_core                     | 2.05 sec                                                               | 2.35 sec: 1.15x slower                                                   |
| xml_etree_generate         | 84.5 ms                                                                | 98.4 ms: 1.16x slower                                                    |
| coroutines                 | 21.6 ms                                                                | 25.3 ms: 1.17x slower                                                    |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                    |
| bpe_tokeniser              | 4.24 sec                                                               | 4.98 sec: 1.18x slower                                                   |
| dulwich_log                | 76.6 ms                                                                | 91.5 ms: 1.20x slower                                                    |
| sphinx                     | 992 ms                                                                 | 1.19 sec: 1.20x slower                                                   |
| scimark_fft                | 314 ms                                                                 | 376 ms: 1.20x slower                                                     |
| bench_mp_pool              | 88.9 ms                                                                | 107 ms: 1.21x slower                                                     |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 587 ms: 1.21x slower                                                     |
| nqueens                    | 80.3 ms                                                                | 97.9 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.35 ms: 1.22x slower                                                    |
| docutils                   | 2.55 sec                                                               | 3.12 sec: 1.22x slower                                                   |
| telco                      | 7.18 ms                                                                | 8.79 ms: 1.22x slower                                                    |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 613 ms: 1.23x slower                                                     |
| many_optionals             | 1.02 ms                                                                | 1.26 ms: 1.23x slower                                                    |
| mdp                        | 2.33 sec                                                               | 2.87 sec: 1.23x slower                                                   |
| async_tree_io_tg           | 610 ms                                                                 | 759 ms: 1.24x slower                                                     |
| deepcopy                   | 256 us                                                                 | 321 us: 1.25x slower                                                     |
| connected_components       | 398 ms                                                                 | 501 ms: 1.26x slower                                                     |
| async_tree_io              | 627 ms                                                                 | 789 ms: 1.26x slower                                                     |
| xml_etree_process          | 58.8 ms                                                                | 74.3 ms: 1.26x slower                                                    |
| shortest_path              | 438 ms                                                                 | 554 ms: 1.26x slower                                                     |
| coverage                   | 79.2 ms                                                                | 100 ms: 1.27x slower                                                     |
| sqlglot_optimize           | 52.1 ms                                                                | 66.1 ms: 1.27x slower                                                    |
| json_dumps                 | 11.3 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| async_generators           | 352 ms                                                                 | 450 ms: 1.28x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.44 sec: 1.29x slower                                                   |
| genshi_xml                 | 49.7 ms                                                                | 64.0 ms: 1.29x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.29x slower                                                     |
| tomli_loads                | 1.97 sec                                                               | 2.56 sec: 1.30x slower                                                   |
| sqlglot_normalize          | 103 ms                                                                 | 134 ms: 1.30x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 334 ms: 1.30x slower                                                     |
| fannkuch                   | 372 ms                                                                 | 487 ms: 1.31x slower                                                     |
| typing_runtime_protocols   | 155 us                                                                 | 204 us: 1.32x slower                                                     |
| pylint                     | 280 ms                                                                 | 369 ms: 1.32x slower                                                     |
| deepcopy_reduce            | 2.60 us                                                                | 3.45 us: 1.32x slower                                                    |
| subparsers                 | 22.2 ms                                                                | 29.6 ms: 1.33x slower                                                    |
| async_tree_none            | 277 ms                                                                 | 368 ms: 1.33x slower                                                     |
| deepcopy_memo              | 30.1 us                                                                | 40.5 us: 1.34x slower                                                    |
| async_tree_memoization     | 332 ms                                                                 | 446 ms: 1.34x slower                                                     |
| thrift                     | 738 us                                                                 | 1.00 ms: 1.36x slower                                                    |
| async_tree_memoization_tg  | 307 ms                                                                 | 417 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                    |
| regex_compile              | 127 ms                                                                 | 174 ms: 1.37x slower                                                     |
| crypto_pyaes               | 65.4 ms                                                                | 90.6 ms: 1.39x slower                                                    |
| pprint_safe_repr           | 710 ms                                                                 | 987 ms: 1.39x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 2.04 sec: 1.41x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 30.7 ms: 1.42x slower                                                    |
| nbody                      | 90.3 ms                                                                | 130 ms: 1.44x slower                                                     |
| 2to3                       | 256 ms                                                                 | 371 ms: 1.45x slower                                                     |
| django_template            | 35.4 ms                                                                | 51.6 ms: 1.46x slower                                                    |
| float                      | 76.4 ms                                                                | 112 ms: 1.47x slower                                                     |
| mako                       | 11.6 ms                                                                | 17.1 ms: 1.48x slower                                                    |
| sqlalchemy_imperative      | 19.1 ms                                                                | 28.2 ms: 1.48x slower                                                    |
| generators                 | 27.1 ms                                                                | 40.1 ms: 1.48x slower                                                    |
| sympy_integrate            | 19.9 ms                                                                | 29.7 ms: 1.49x slower                                                    |
| logging_format             | 6.79 us                                                                | 10.3 us: 1.51x slower                                                    |
| logging_simple             | 6.14 us                                                                | 9.28 us: 1.51x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 198 ms: 1.57x slower                                                     |
| pyflate                    | 421 ms                                                                 | 681 ms: 1.62x slower                                                     |
| unpickle_pure_python       | 213 us                                                                 | 346 us: 1.63x slower                                                     |
| richards_super             | 50.7 ms                                                                | 83.0 ms: 1.64x slower                                                    |
| pickle_pure_python         | 323 us                                                                 | 535 us: 1.65x slower                                                     |
| comprehensions             | 17.2 us                                                                | 28.7 us: 1.67x slower                                                    |
| richards                   | 44.7 ms                                                                | 75.2 ms: 1.68x slower                                                    |
| scimark_lu                 | 110 ms                                                                 | 189 ms: 1.72x slower                                                     |
| chaos                      | 58.4 ms                                                                | 101 ms: 1.73x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 2.73 ms: 1.75x slower                                                    |
| scimark_monte_carlo        | 64.7 ms                                                                | 113 ms: 1.75x slower                                                     |
| hexiom                     | 5.84 ms                                                                | 10.2 ms: 1.75x slower                                                    |
| sympy_str                  | 271 ms                                                                 | 476 ms: 1.76x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                                | 2.37 ms: 1.89x slower                                                    |
| logging_silent             | 106 ns                                                                 | 201 ns: 1.90x slower                                                     |
| scimark_sor                | 128 ms                                                                 | 245 ms: 1.92x slower                                                     |
| raytrace                   | 260 ms                                                                 | 534 ms: 2.05x slower                                                     |
| sympy_expand               | 453 ms                                                                 | 954 ms: 2.11x slower                                                     |
| go                         | 117 ms                                                                 | 267 ms: 2.28x slower                                                     |
| sympy_sum                  | 152 ms                                                                 | 349 ms: 2.30x slower                                                     |
| deltablue                  | 3.17 ms                                                                | 8.28 ms: 2.61x slower                                                    |
| bench_thread_pool          | 1.04 ms                                                                | 3.40 ms: 3.27x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, regex_v8
Ignored benchmarks (1) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: html5lib

- Geometric mean (including insignificant results): 1.262x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x