# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.145x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 316 ms: 1.24x slower                                                 |
| docutils       | 2.55 sec                                                               | 2.83 sec: 1.11x slower                                               |
| sphinx         | 992 ms                                                                 | 1.11 sec: 1.12x slower                                               |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                                 | 238 ms: 1.09x faster                                                 |
| async_tree_io_tg           | 622 ms                                                                 | 588 ms: 1.06x faster                                                 |
| async_tree_io              | 630 ms                                                                 | 600 ms: 1.05x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                 |
| coroutines                 | 22.7 ms                                                                | 22.6 ms: 1.00x faster                                                |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                 | 486 ms: 1.01x slower                                                 |
| async_tree_none            | 279 ms                                                                 | 282 ms: 1.01x slower                                                 |
| async_tree_memoization     | 336 ms                                                                 | 346 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 498 ms                                                                 | 519 ms: 1.04x slower                                                 |
| async_generators           | 354 ms                                                                 | 413 ms: 1.17x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                 |
| float          | 77.0 ms                                                                | 79.1 ms: 1.03x slower                                                |
| nbody          | 91.2 ms                                                                | 129 ms: 1.41x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 23.9 ms: 1.02x slower                                                |
| regex_dna      | 167 ms                                                                 | 172 ms: 1.03x slower                                                 |
| regex_effbot   | 2.70 ms                                                                | 2.84 ms: 1.05x slower                                                |
| regex_compile  | 126 ms                                                                 | 148 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.9 ms                                                                | 88.1 ms: 1.03x faster                                                |
| xml_etree_parse      | 128 ms                                                                 | 131 ms: 1.02x slower                                                 |
| json_loads           | 25.9 us                                                                | 28.2 us: 1.09x slower                                                |
| pickle_pure_python   | 322 us                                                                 | 357 us: 1.11x slower                                                 |
| unpickle_pure_python | 212 us                                                                 | 239 us: 1.13x slower                                                 |
| xml_etree_generate   | 83.7 ms                                                                | 95.3 ms: 1.14x slower                                                |
| json_dumps           | 11.5 ms                                                                | 13.1 ms: 1.14x slower                                                |
| xml_etree_process    | 58.3 ms                                                                | 67.5 ms: 1.16x slower                                                |
| tomli_loads          | 1.97 sec                                                               | 2.33 sec: 1.18x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.0 ms: 1.17x slower                                                |
| python_startup_no_site | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.4 ms                                                                | 59.7 ms: 1.21x slower                                                |
| django_template | 35.4 ms                                                                | 43.3 ms: 1.22x slower                                                |
| genshi_text     | 21.5 ms                                                                | 27.7 ms: 1.29x slower                                                |
| mako            | 11.6 ms                                                                | 15.4 ms: 1.33x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.26x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 4.59 ms                                                                | 3.52 ms: 1.31x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 2.05 us: 1.10x faster                                                |
| async_tree_none_tg         | 258 ms                                                                 | 238 ms: 1.09x faster                                                 |
| async_tree_io_tg           | 622 ms                                                                 | 588 ms: 1.06x faster                                                 |
| async_tree_io              | 630 ms                                                                 | 600 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 90.9 ms                                                                | 88.1 ms: 1.03x faster                                                |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                 |
| coroutines                 | 22.7 ms                                                                | 22.6 ms: 1.00x faster                                                |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                 | 486 ms: 1.01x slower                                                 |
| async_tree_none            | 279 ms                                                                 | 282 ms: 1.01x slower                                                 |
| regex_v8                   | 23.5 ms                                                                | 23.9 ms: 1.02x slower                                                |
| xml_etree_parse            | 128 ms                                                                 | 131 ms: 1.02x slower                                                 |
| float                      | 77.0 ms                                                                | 79.1 ms: 1.03x slower                                                |
| async_tree_memoization     | 336 ms                                                                 | 346 ms: 1.03x slower                                                 |
| regex_dna                  | 167 ms                                                                 | 172 ms: 1.03x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.03x slower                                                |
| async_tree_cpu_io_mixed    | 498 ms                                                                 | 519 ms: 1.04x slower                                                 |
| json                       | 4.74 ms                                                                | 4.94 ms: 1.04x slower                                                |
| regex_effbot               | 2.70 ms                                                                | 2.84 ms: 1.05x slower                                                |
| dulwich_log                | 75.4 ms                                                                | 81.0 ms: 1.07x slower                                                |
| json_loads                 | 25.9 us                                                                | 28.2 us: 1.09x slower                                                |
| pycparser                  | 1.11 sec                                                               | 1.22 sec: 1.09x slower                                               |
| logging_silent             | 107 ns                                                                 | 118 ns: 1.10x slower                                                 |
| spectral_norm              | 99.1 ms                                                                | 109 ms: 1.10x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.58 sec: 1.11x slower                                               |
| docutils                   | 2.55 sec                                                               | 2.83 sec: 1.11x slower                                               |
| pyflate                    | 434 ms                                                                 | 481 ms: 1.11x slower                                                 |
| pickle_pure_python         | 322 us                                                                 | 357 us: 1.11x slower                                                 |
| bpe_tokeniser              | 4.26 sec                                                               | 4.74 sec: 1.11x slower                                               |
| sphinx                     | 992 ms                                                                 | 1.11 sec: 1.12x slower                                               |
| k_core                     | 2.06 sec                                                               | 2.31 sec: 1.12x slower                                               |
| unpickle_pure_python       | 212 us                                                                 | 239 us: 1.13x slower                                                 |
| generators                 | 27.1 ms                                                                | 30.5 ms: 1.13x slower                                                |
| many_optionals             | 1.02 ms                                                                | 1.16 ms: 1.14x slower                                                |
| xml_etree_generate         | 83.7 ms                                                                | 95.3 ms: 1.14x slower                                                |
| json_dumps                 | 11.5 ms                                                                | 13.1 ms: 1.14x slower                                                |
| subparsers                 | 22.4 ms                                                                | 25.6 ms: 1.14x slower                                                |
| go                         | 118 ms                                                                 | 134 ms: 1.14x slower                                                 |
| xml_etree_process          | 58.3 ms                                                                | 67.5 ms: 1.16x slower                                                |
| sqlglot_normalize          | 103 ms                                                                 | 120 ms: 1.16x slower                                                 |
| python_startup             | 14.6 ms                                                                | 17.0 ms: 1.17x slower                                                |
| async_generators           | 354 ms                                                                 | 413 ms: 1.17x slower                                                 |
| regex_compile              | 126 ms                                                                 | 148 ms: 1.17x slower                                                 |
| scimark_fft                | 315 ms                                                                 | 369 ms: 1.17x slower                                                 |
| telco                      | 7.26 ms                                                                | 8.51 ms: 1.17x slower                                                |
| sqlglot_optimize           | 52.0 ms                                                                | 61.0 ms: 1.17x slower                                                |
| chaos                      | 58.5 ms                                                                | 69.0 ms: 1.18x slower                                                |
| tomli_loads                | 1.97 sec                                                               | 2.33 sec: 1.18x slower                                               |
| pprint_safe_repr           | 713 ms                                                                 | 844 ms: 1.18x slower                                                 |
| scimark_sor                | 125 ms                                                                 | 148 ms: 1.19x slower                                                 |
| logging_simple             | 6.16 us                                                                | 7.30 us: 1.19x slower                                                |
| bench_mp_pool              | 88.5 ms                                                                | 105 ms: 1.19x slower                                                 |
| comprehensions             | 17.0 us                                                                | 20.4 us: 1.20x slower                                                |
| sqlglot_transpile          | 1.59 ms                                                                | 1.91 ms: 1.20x slower                                                |
| pprint_pformat             | 1.45 sec                                                               | 1.74 sec: 1.20x slower                                               |
| raytrace                   | 262 ms                                                                 | 315 ms: 1.20x slower                                                 |
| genshi_xml                 | 49.4 ms                                                                | 59.7 ms: 1.21x slower                                                |
| deepcopy                   | 255 us                                                                 | 309 us: 1.21x slower                                                 |
| logging_format             | 6.91 us                                                                | 8.38 us: 1.21x slower                                                |
| connected_components       | 399 ms                                                                 | 486 ms: 1.22x slower                                                 |
| pylint                     | 280 ms                                                                 | 341 ms: 1.22x slower                                                 |
| django_template            | 35.4 ms                                                                | 43.3 ms: 1.22x slower                                                |
| thrift                     | 740 us                                                                 | 906 us: 1.23x slower                                                 |
| nqueens                    | 77.9 ms                                                                | 95.7 ms: 1.23x slower                                                |
| richards                   | 45.1 ms                                                                | 55.7 ms: 1.24x slower                                                |
| deepcopy_reduce            | 2.61 us                                                                | 3.24 us: 1.24x slower                                                |
| sqlglot_parse              | 1.28 ms                                                                | 1.58 ms: 1.24x slower                                                |
| 2to3                       | 255 ms                                                                 | 316 ms: 1.24x slower                                                 |
| shortest_path              | 439 ms                                                                 | 546 ms: 1.24x slower                                                 |
| hexiom                     | 5.91 ms                                                                | 7.41 ms: 1.25x slower                                                |
| coverage                   | 79.2 ms                                                                | 99.3 ms: 1.25x slower                                                |
| scimark_monte_carlo        | 63.6 ms                                                                | 80.0 ms: 1.26x slower                                                |
| richards_super             | 50.9 ms                                                                | 64.5 ms: 1.27x slower                                                |
| crypto_pyaes               | 68.1 ms                                                                | 86.4 ms: 1.27x slower                                                |
| typing_runtime_protocols   | 155 us                                                                 | 198 us: 1.28x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 24.3 ms: 1.28x slower                                                |
| meteor_contest             | 99.9 ms                                                                | 128 ms: 1.28x slower                                                 |
| deepcopy_memo              | 29.9 us                                                                | 38.4 us: 1.28x slower                                                |
| genshi_text                | 21.5 ms                                                                | 27.7 ms: 1.29x slower                                                |
| scimark_sparse_mat_mult    | 4.15 ms                                                                | 5.38 ms: 1.30x slower                                                |
| fannkuch                   | 367 ms                                                                 | 479 ms: 1.31x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.4 ms: 1.33x slower                                                |
| python_startup_no_site     | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                |
| sqlalchemy_declarative     | 126 ms                                                                 | 176 ms: 1.40x slower                                                 |
| nbody                      | 91.2 ms                                                                | 129 ms: 1.41x slower                                                 |
| deltablue                  | 3.23 ms                                                                | 4.62 ms: 1.43x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 28.3 ms: 1.43x slower                                                |
| scimark_lu                 | 110 ms                                                                 | 167 ms: 1.51x slower                                                 |
| sympy_str                  | 270 ms                                                                 | 455 ms: 1.68x slower                                                 |
| sympy_expand               | 456 ms                                                                 | 924 ms: 2.03x slower                                                 |
| sympy_sum                  | 152 ms                                                                 | 339 ms: 2.24x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.32 ms: 3.21x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.18x slower                                                         |

Benchmark hidden because not significant (2): create_gc_cycles, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: html5lib

- Geometric mean (including insignificant results): 1.145x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x