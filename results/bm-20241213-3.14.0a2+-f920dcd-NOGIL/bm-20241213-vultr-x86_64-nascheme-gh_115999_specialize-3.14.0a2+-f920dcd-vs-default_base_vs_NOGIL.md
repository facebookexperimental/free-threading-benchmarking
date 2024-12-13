# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: f920dcd
- commit date: 2024-12-13
- overall geometric mean: 1.257x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 366 ms: 1.45x slower                                                     |
| docutils       | 2.53 sec                                                               | 3.08 sec: 1.22x slower                                                   |
| sphinx         | 980 ms                                                                 | 1.18 sec: 1.21x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 583 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 612 ms: 1.08x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 24.5 ms: 1.15x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 763 ms: 1.25x slower                                                     |
| async_generators           | 359 ms                                                                 | 449 ms: 1.25x slower                                                     |
| async_tree_io              | 625 ms                                                                 | 788 ms: 1.26x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 328 ms: 1.29x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 363 ms: 1.31x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 444 ms: 1.34x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 416 ms: 1.36x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.21x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 181 ms: 1.19x faster                                                     |
| nbody          | 89.4 ms                                                                | 130 ms: 1.45x slower                                                     |
| float          | 77.2 ms                                                                | 115 ms: 1.49x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.22x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 24.4 ms: 1.01x faster                                                    |
| regex_effbot   | 2.68 ms                                                                | 2.77 ms: 1.03x slower                                                    |
| regex_dna      | 172 ms                                                                 | 181 ms: 1.05x slower                                                     |
| regex_compile  | 127 ms                                                                 | 173 ms: 1.36x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.02x slower                                                     |
| json_loads           | 26.5 us                                                                | 28.4 us: 1.07x slower                                                    |
| xml_etree_generate   | 82.9 ms                                                                | 97.2 ms: 1.17x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.2 ms: 1.25x slower                                                    |
| tomli_loads          | 2.06 sec                                                               | 2.61 sec: 1.27x slower                                                   |
| xml_etree_process    | 57.8 ms                                                                | 73.7 ms: 1.28x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 329 us: 1.58x slower                                                     |
| pickle_pure_python   | 314 us                                                                 | 503 us: 1.60x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                    |
| python_startup_no_site | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 63.9 ms: 1.29x slower                                                    |
| django_template | 34.6 ms                                                                | 50.5 ms: 1.46x slower                                                    |
| genshi_text     | 21.4 ms                                                                | 31.6 ms: 1.48x slower                                                    |
| mako            | 11.4 ms                                                                | 17.5 ms: 1.53x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.44x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.62 ms                                                                | 3.51 ms: 1.32x faster                                                    |
| pidigits                   | 216 ms                                                                 | 181 ms: 1.19x faster                                                     |
| create_gc_cycles           | 1.85 ms                                                                | 1.83 ms: 1.01x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                     |
| regex_v8                   | 24.5 ms                                                                | 24.4 ms: 1.01x faster                                                    |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.02x slower                                                     |
| regex_effbot               | 2.68 ms                                                                | 2.77 ms: 1.03x slower                                                    |
| regex_dna                  | 172 ms                                                                 | 181 ms: 1.05x slower                                                     |
| json                       | 4.81 ms                                                                | 5.07 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 583 ms: 1.07x slower                                                     |
| json_loads                 | 26.5 us                                                                | 28.4 us: 1.07x slower                                                    |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 612 ms: 1.08x slower                                                     |
| pathlib                    | 18.4 ms                                                                | 20.0 ms: 1.09x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 123 ms: 1.15x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 24.5 ms: 1.15x slower                                                    |
| xml_etree_generate         | 82.9 ms                                                                | 97.2 ms: 1.17x slower                                                    |
| bpe_tokeniser              | 4.23 sec                                                               | 4.97 sec: 1.18x slower                                                   |
| k_core                     | 2.06 sec                                                               | 2.42 sec: 1.18x slower                                                   |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                    |
| telco                      | 7.26 ms                                                                | 8.69 ms: 1.20x slower                                                    |
| sphinx                     | 980 ms                                                                 | 1.18 sec: 1.21x slower                                                   |
| docutils                   | 2.53 sec                                                               | 3.08 sec: 1.22x slower                                                   |
| bench_mp_pool              | 88.9 ms                                                                | 108 ms: 1.22x slower                                                     |
| dulwich_log                | 74.8 ms                                                                | 92.5 ms: 1.24x slower                                                    |
| mdp                        | 2.34 sec                                                               | 2.90 sec: 1.24x slower                                                   |
| scimark_fft                | 323 ms                                                                 | 401 ms: 1.24x slower                                                     |
| nqueens                    | 78.8 ms                                                                | 98.1 ms: 1.24x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 763 ms: 1.25x slower                                                     |
| async_generators           | 359 ms                                                                 | 449 ms: 1.25x slower                                                     |
| shortest_path              | 439 ms                                                                 | 549 ms: 1.25x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 14.2 ms: 1.25x slower                                                    |
| connected_components       | 398 ms                                                                 | 500 ms: 1.26x slower                                                     |
| async_tree_io              | 625 ms                                                                 | 788 ms: 1.26x slower                                                     |
| tomli_loads                | 2.06 sec                                                               | 2.61 sec: 1.27x slower                                                   |
| many_optionals             | 1.01 ms                                                                | 1.28 ms: 1.27x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.42 sec: 1.27x slower                                                   |
| xml_etree_process          | 57.8 ms                                                                | 73.7 ms: 1.28x slower                                                    |
| async_tree_none_tg         | 255 ms                                                                 | 328 ms: 1.29x slower                                                     |
| genshi_xml                 | 49.3 ms                                                                | 63.9 ms: 1.29x slower                                                    |
| deepcopy                   | 252 us                                                                 | 327 us: 1.30x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 130 ms: 1.30x slower                                                     |
| typing_runtime_protocols   | 154 us                                                                 | 201 us: 1.30x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 134 ms: 1.30x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 363 ms: 1.31x slower                                                     |
| coverage                   | 78.1 ms                                                                | 103 ms: 1.31x slower                                                     |
| sqlglot_optimize           | 51.7 ms                                                                | 68.6 ms: 1.33x slower                                                    |
| fannkuch                   | 375 ms                                                                 | 498 ms: 1.33x slower                                                     |
| deepcopy_memo              | 29.7 us                                                                | 39.4 us: 1.33x slower                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 3.47 us: 1.34x slower                                                    |
| async_tree_memoization     | 332 ms                                                                 | 444 ms: 1.34x slower                                                     |
| pprint_safe_repr           | 708 ms                                                                 | 955 ms: 1.35x slower                                                     |
| crypto_pyaes               | 68.0 ms                                                                | 91.9 ms: 1.35x slower                                                    |
| pylint                     | 278 ms                                                                 | 376 ms: 1.35x slower                                                     |
| regex_compile              | 127 ms                                                                 | 173 ms: 1.36x slower                                                     |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.95 ms: 1.36x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 416 ms: 1.36x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.98 sec: 1.36x slower                                                   |
| python_startup_no_site     | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| subparsers                 | 21.5 ms                                                                | 30.4 ms: 1.41x slower                                                    |
| generators                 | 26.6 ms                                                                | 38.3 ms: 1.44x slower                                                    |
| 2to3                       | 253 ms                                                                 | 366 ms: 1.45x slower                                                     |
| nbody                      | 89.4 ms                                                                | 130 ms: 1.45x slower                                                     |
| thrift                     | 726 us                                                                 | 1.06 ms: 1.46x slower                                                    |
| django_template            | 34.6 ms                                                                | 50.5 ms: 1.46x slower                                                    |
| genshi_text                | 21.4 ms                                                                | 31.6 ms: 1.48x slower                                                    |
| float                      | 77.2 ms                                                                | 115 ms: 1.49x slower                                                     |
| richards_super             | 51.3 ms                                                                | 76.2 ms: 1.49x slower                                                    |
| richards                   | 45.3 ms                                                                | 67.8 ms: 1.50x slower                                                    |
| sympy_integrate            | 19.6 ms                                                                | 29.5 ms: 1.50x slower                                                    |
| sqlalchemy_imperative      | 18.8 ms                                                                | 28.3 ms: 1.50x slower                                                    |
| mako                       | 11.4 ms                                                                | 17.5 ms: 1.53x slower                                                    |
| pyflate                    | 439 ms                                                                 | 676 ms: 1.54x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 329 us: 1.58x slower                                                     |
| sqlalchemy_declarative     | 126 ms                                                                 | 199 ms: 1.59x slower                                                     |
| comprehensions             | 17.0 us                                                                | 27.2 us: 1.60x slower                                                    |
| pickle_pure_python         | 314 us                                                                 | 503 us: 1.60x slower                                                     |
| logging_format             | 6.78 us                                                                | 11.3 us: 1.66x slower                                                    |
| hexiom                     | 5.78 ms                                                                | 9.72 ms: 1.68x slower                                                    |
| chaos                      | 57.5 ms                                                                | 97.2 ms: 1.69x slower                                                    |
| logging_simple             | 5.95 us                                                                | 10.1 us: 1.69x slower                                                    |
| scimark_monte_carlo        | 63.7 ms                                                                | 108 ms: 1.70x slower                                                     |
| scimark_lu                 | 107 ms                                                                 | 183 ms: 1.70x slower                                                     |
| logging_silent             | 106 ns                                                                 | 185 ns: 1.74x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 2.74 ms: 1.75x slower                                                    |
| sympy_str                  | 268 ms                                                                 | 474 ms: 1.77x slower                                                     |
| scimark_sor                | 131 ms                                                                 | 235 ms: 1.79x slower                                                     |
| sqlglot_parse              | 1.26 ms                                                                | 2.37 ms: 1.88x slower                                                    |
| raytrace                   | 259 ms                                                                 | 498 ms: 1.93x slower                                                     |
| go                         | 117 ms                                                                 | 245 ms: 2.10x slower                                                     |
| sympy_expand               | 451 ms                                                                 | 950 ms: 2.11x slower                                                     |
| sympy_sum                  | 151 ms                                                                 | 348 ms: 2.30x slower                                                     |
| deltablue                  | 3.16 ms                                                                | 7.49 ms: 2.37x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.43 ms: 3.34x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.36x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, sqlite_synth
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd.json: html5lib

- Geometric mean (including insignificant results): 1.257x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x