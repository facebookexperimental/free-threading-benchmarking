# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.258x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 367 ms: 1.44x slower                                                     |
| docutils       | 2.55 sec                                                               | 3.07 sec: 1.20x slower                                                   |
| sphinx         | 992 ms                                                                 | 1.17 sec: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                     |
| coroutines                 | 21.6 ms                                                                | 25.1 ms: 1.16x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 583 ms: 1.20x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 608 ms: 1.22x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 752 ms: 1.23x slower                                                     |
| async_tree_io              | 627 ms                                                                 | 777 ms: 1.24x slower                                                     |
| async_generators           | 352 ms                                                                 | 446 ms: 1.27x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 327 ms: 1.28x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 363 ms: 1.31x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 442 ms: 1.33x slower                                                     |
| async_tree_memoization_tg  | 307 ms                                                                 | 415 ms: 1.35x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.23x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 90.3 ms                                                                | 131 ms: 1.45x slower                                                     |
| float          | 76.4 ms                                                                | 111 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 24.8 ms: 1.02x slower                                                    |
| regex_effbot   | 2.69 ms                                                                | 2.79 ms: 1.04x slower                                                    |
| regex_dna      | 175 ms                                                                 | 188 ms: 1.08x slower                                                     |
| regex_compile  | 127 ms                                                                 | 172 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 89.9 ms: 1.01x faster                                                    |
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.02x slower                                                     |
| json_loads           | 26.1 us                                                                | 28.5 us: 1.09x slower                                                    |
| xml_etree_generate   | 84.5 ms                                                                | 98.3 ms: 1.16x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.2 ms: 1.26x slower                                                    |
| xml_etree_process    | 58.8 ms                                                                | 74.3 ms: 1.26x slower                                                    |
| tomli_loads          | 1.97 sec                                                               | 2.59 sec: 1.32x slower                                                   |
| unpickle_pure_python | 213 us                                                                 | 346 us: 1.63x slower                                                     |
| pickle_pure_python   | 323 us                                                                 | 533 us: 1.65x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                             |

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
| genshi_xml      | 49.7 ms                                                                | 63.5 ms: 1.28x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 30.6 ms: 1.41x slower                                                    |
| django_template | 35.4 ms                                                                | 51.2 ms: 1.45x slower                                                    |
| mako            | 11.6 ms                                                                | 17.2 ms: 1.48x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                | 3.16 ms: 1.35x faster                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.14 us: 1.03x faster                                                    |
| create_gc_cycles           | 1.83 ms                                                                | 1.78 ms: 1.02x faster                                                    |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                     |
| xml_etree_iterparse        | 90.6 ms                                                                | 89.9 ms: 1.01x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                     |
| regex_v8                   | 24.4 ms                                                                | 24.8 ms: 1.02x slower                                                    |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.02x slower                                                     |
| regex_effbot               | 2.69 ms                                                                | 2.79 ms: 1.04x slower                                                    |
| json                       | 4.76 ms                                                                | 5.05 ms: 1.06x slower                                                    |
| regex_dna                  | 175 ms                                                                 | 188 ms: 1.08x slower                                                     |
| pathlib                    | 18.2 ms                                                                | 19.6 ms: 1.08x slower                                                    |
| json_loads                 | 26.1 us                                                                | 28.5 us: 1.09x slower                                                    |
| spectral_norm              | 96.3 ms                                                                | 107 ms: 1.12x slower                                                     |
| k_core                     | 2.05 sec                                                               | 2.36 sec: 1.15x slower                                                   |
| coroutines                 | 21.6 ms                                                                | 25.1 ms: 1.16x slower                                                    |
| xml_etree_generate         | 84.5 ms                                                                | 98.3 ms: 1.16x slower                                                    |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                    |
| bpe_tokeniser              | 4.24 sec                                                               | 4.99 sec: 1.18x slower                                                   |
| sphinx                     | 992 ms                                                                 | 1.17 sec: 1.18x slower                                                   |
| scimark_fft                | 314 ms                                                                 | 371 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.20 ms: 1.19x slower                                                    |
| dulwich_log                | 76.6 ms                                                                | 91.2 ms: 1.19x slower                                                    |
| telco                      | 7.18 ms                                                                | 8.58 ms: 1.19x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 583 ms: 1.20x slower                                                     |
| docutils                   | 2.55 sec                                                               | 3.07 sec: 1.20x slower                                                   |
| bench_mp_pool              | 88.9 ms                                                                | 107 ms: 1.21x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 608 ms: 1.22x slower                                                     |
| nqueens                    | 80.3 ms                                                                | 97.8 ms: 1.22x slower                                                    |
| many_optionals             | 1.02 ms                                                                | 1.25 ms: 1.22x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 752 ms: 1.23x slower                                                     |
| mdp                        | 2.33 sec                                                               | 2.88 sec: 1.24x slower                                                   |
| async_tree_io              | 627 ms                                                                 | 777 ms: 1.24x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 14.2 ms: 1.26x slower                                                    |
| xml_etree_process          | 58.8 ms                                                                | 74.3 ms: 1.26x slower                                                    |
| connected_components       | 398 ms                                                                 | 503 ms: 1.26x slower                                                     |
| async_generators           | 352 ms                                                                 | 446 ms: 1.27x slower                                                     |
| shortest_path              | 438 ms                                                                 | 556 ms: 1.27x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.43 sec: 1.27x slower                                                   |
| sqlglot_optimize           | 52.1 ms                                                                | 66.3 ms: 1.27x slower                                                    |
| deepcopy                   | 256 us                                                                 | 327 us: 1.28x slower                                                     |
| genshi_xml                 | 49.7 ms                                                                | 63.5 ms: 1.28x slower                                                    |
| async_tree_none_tg         | 256 ms                                                                 | 327 ms: 1.28x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.29x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 133 ms: 1.30x slower                                                     |
| typing_runtime_protocols   | 155 us                                                                 | 202 us: 1.30x slower                                                     |
| pylint                     | 280 ms                                                                 | 367 ms: 1.31x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 363 ms: 1.31x slower                                                     |
| tomli_loads                | 1.97 sec                                                               | 2.59 sec: 1.32x slower                                                   |
| coverage                   | 79.2 ms                                                                | 105 ms: 1.32x slower                                                     |
| fannkuch                   | 372 ms                                                                 | 493 ms: 1.33x slower                                                     |
| deepcopy_reduce            | 2.60 us                                                                | 3.46 us: 1.33x slower                                                    |
| async_tree_memoization     | 332 ms                                                                 | 442 ms: 1.33x slower                                                     |
| subparsers                 | 22.2 ms                                                                | 29.7 ms: 1.33x slower                                                    |
| deepcopy_memo              | 30.1 us                                                                | 40.2 us: 1.33x slower                                                    |
| async_tree_memoization_tg  | 307 ms                                                                 | 415 ms: 1.35x slower                                                     |
| regex_compile              | 127 ms                                                                 | 172 ms: 1.35x slower                                                     |
| thrift                     | 738 us                                                                 | 998 us: 1.35x slower                                                     |
| python_startup_no_site     | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                    |
| pprint_safe_repr           | 710 ms                                                                 | 984 ms: 1.39x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 2.04 sec: 1.41x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 30.6 ms: 1.41x slower                                                    |
| crypto_pyaes               | 65.4 ms                                                                | 92.7 ms: 1.42x slower                                                    |
| 2to3                       | 256 ms                                                                 | 367 ms: 1.44x slower                                                     |
| django_template            | 35.4 ms                                                                | 51.2 ms: 1.45x slower                                                    |
| nbody                      | 90.3 ms                                                                | 131 ms: 1.45x slower                                                     |
| generators                 | 27.1 ms                                                                | 39.5 ms: 1.46x slower                                                    |
| float                      | 76.4 ms                                                                | 111 ms: 1.46x slower                                                     |
| sqlalchemy_imperative      | 19.1 ms                                                                | 28.2 ms: 1.48x slower                                                    |
| mako                       | 11.6 ms                                                                | 17.2 ms: 1.48x slower                                                    |
| sympy_integrate            | 19.9 ms                                                                | 29.5 ms: 1.49x slower                                                    |
| logging_simple             | 6.14 us                                                                | 9.35 us: 1.52x slower                                                    |
| logging_format             | 6.79 us                                                                | 10.5 us: 1.54x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 198 ms: 1.56x slower                                                     |
| pyflate                    | 421 ms                                                                 | 672 ms: 1.60x slower                                                     |
| richards_super             | 50.7 ms                                                                | 81.6 ms: 1.61x slower                                                    |
| unpickle_pure_python       | 213 us                                                                 | 346 us: 1.63x slower                                                     |
| richards                   | 44.7 ms                                                                | 73.6 ms: 1.65x slower                                                    |
| pickle_pure_python         | 323 us                                                                 | 533 us: 1.65x slower                                                     |
| comprehensions             | 17.2 us                                                                | 28.5 us: 1.65x slower                                                    |
| chaos                      | 58.4 ms                                                                | 99.0 ms: 1.70x slower                                                    |
| scimark_lu                 | 110 ms                                                                 | 187 ms: 1.70x slower                                                     |
| scimark_monte_carlo        | 64.7 ms                                                                | 111 ms: 1.72x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 2.71 ms: 1.73x slower                                                    |
| sympy_str                  | 271 ms                                                                 | 473 ms: 1.75x slower                                                     |
| hexiom                     | 5.84 ms                                                                | 10.2 ms: 1.75x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 2.35 ms: 1.88x slower                                                    |
| logging_silent             | 106 ns                                                                 | 200 ns: 1.89x slower                                                     |
| scimark_sor                | 128 ms                                                                 | 245 ms: 1.92x slower                                                     |
| raytrace                   | 260 ms                                                                 | 523 ms: 2.01x slower                                                     |
| sympy_expand               | 453 ms                                                                 | 953 ms: 2.10x slower                                                     |
| go                         | 117 ms                                                                 | 261 ms: 2.23x slower                                                     |
| sympy_sum                  | 152 ms                                                                 | 348 ms: 2.29x slower                                                     |
| deltablue                  | 3.17 ms                                                                | 8.05 ms: 2.54x slower                                                    |
| bench_thread_pool          | 1.04 ms                                                                | 3.39 ms: 3.27x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.36x slower                                                             |
Ignored benchmarks (1) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: html5lib

- Geometric mean (including insignificant results): 1.258x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x