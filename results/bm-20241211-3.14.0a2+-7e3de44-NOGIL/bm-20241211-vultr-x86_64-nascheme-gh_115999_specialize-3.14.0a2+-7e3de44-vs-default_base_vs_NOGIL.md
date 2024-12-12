# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 7e3de44
- commit date: 2024-12-11
- overall geometric mean: 1.270x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 367 ms: 1.45x slower                                                     |
| docutils       | 2.53 sec                                                               | 3.07 sec: 1.21x slower                                                   |
| sphinx         | 980 ms                                                                 | 1.19 sec: 1.21x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 612 ms: 1.08x slower                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 594 ms: 1.09x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 24.9 ms: 1.17x slower                                                    |
| async_generators           | 359 ms                                                                 | 457 ms: 1.27x slower                                                     |
| async_tree_io              | 625 ms                                                                 | 795 ms: 1.27x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 781 ms: 1.28x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 364 ms: 1.31x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 337 ms: 1.32x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 448 ms: 1.35x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 425 ms: 1.39x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.22x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                     |
| nbody          | 89.4 ms                                                                | 129 ms: 1.44x slower                                                     |
| float          | 77.2 ms                                                                | 115 ms: 1.48x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.22x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                    |
| regex_effbot   | 2.68 ms                                                                | 2.93 ms: 1.09x slower                                                    |
| regex_dna      | 172 ms                                                                 | 191 ms: 1.11x slower                                                     |
| regex_compile  | 127 ms                                                                 | 181 ms: 1.43x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| json_loads           | 26.5 us                                                                | 28.5 us: 1.08x slower                                                    |
| xml_etree_generate   | 82.9 ms                                                                | 98.1 ms: 1.18x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| tomli_loads          | 2.06 sec                                                               | 2.62 sec: 1.27x slower                                                   |
| xml_etree_process    | 57.8 ms                                                                | 78.9 ms: 1.37x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 331 us: 1.59x slower                                                     |
| pickle_pure_python   | 314 us                                                                 | 499 us: 1.59x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 63.7 ms: 1.29x slower                                                    |
| django_template | 34.6 ms                                                                | 50.2 ms: 1.45x slower                                                    |
| genshi_text     | 21.4 ms                                                                | 31.5 ms: 1.47x slower                                                    |
| mako            | 11.4 ms                                                                | 17.8 ms: 1.56x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.44x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.62 ms                                                                | 3.51 ms: 1.32x faster                                                    |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                     |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.01x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                     |
| sqlite_synth               | 2.23 us                                                                | 2.28 us: 1.02x slower                                                    |
| xml_etree_parse            | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| regex_v8                   | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                    |
| json                       | 4.81 ms                                                                | 5.05 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 612 ms: 1.08x slower                                                     |
| json_loads                 | 26.5 us                                                                | 28.5 us: 1.08x slower                                                    |
| pathlib                    | 18.4 ms                                                                | 19.8 ms: 1.08x slower                                                    |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 594 ms: 1.09x slower                                                     |
| regex_effbot               | 2.68 ms                                                                | 2.93 ms: 1.09x slower                                                    |
| regex_dna                  | 172 ms                                                                 | 191 ms: 1.11x slower                                                     |
| spectral_norm              | 108 ms                                                                 | 120 ms: 1.12x slower                                                     |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                   |
| coroutines                 | 21.3 ms                                                                | 24.9 ms: 1.17x slower                                                    |
| k_core                     | 2.06 sec                                                               | 2.41 sec: 1.17x slower                                                   |
| bpe_tokeniser              | 4.23 sec                                                               | 4.98 sec: 1.18x slower                                                   |
| xml_etree_generate         | 82.9 ms                                                                | 98.1 ms: 1.18x slower                                                    |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| docutils                   | 2.53 sec                                                               | 3.07 sec: 1.21x slower                                                   |
| sphinx                     | 980 ms                                                                 | 1.19 sec: 1.21x slower                                                   |
| scimark_fft                | 323 ms                                                                 | 396 ms: 1.22x slower                                                     |
| telco                      | 7.26 ms                                                                | 8.89 ms: 1.22x slower                                                    |
| bench_mp_pool              | 88.9 ms                                                                | 109 ms: 1.23x slower                                                     |
| nqueens                    | 78.8 ms                                                                | 98.0 ms: 1.24x slower                                                    |
| dulwich_log                | 74.8 ms                                                                | 93.4 ms: 1.25x slower                                                    |
| shortest_path              | 439 ms                                                                 | 551 ms: 1.26x slower                                                     |
| connected_components       | 398 ms                                                                 | 501 ms: 1.26x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| async_generators           | 359 ms                                                                 | 457 ms: 1.27x slower                                                     |
| async_tree_io              | 625 ms                                                                 | 795 ms: 1.27x slower                                                     |
| tomli_loads                | 2.06 sec                                                               | 2.62 sec: 1.27x slower                                                   |
| many_optionals             | 1.01 ms                                                                | 1.29 ms: 1.28x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 781 ms: 1.28x slower                                                     |
| deepcopy                   | 252 us                                                                 | 324 us: 1.29x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 129 ms: 1.29x slower                                                     |
| genshi_xml                 | 49.3 ms                                                                | 63.7 ms: 1.29x slower                                                    |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.66 ms: 1.29x slower                                                    |
| sqlglot_normalize          | 103 ms                                                                 | 134 ms: 1.30x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 364 ms: 1.31x slower                                                     |
| fannkuch                   | 375 ms                                                                 | 495 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 154 us                                                                 | 204 us: 1.32x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 337 ms: 1.32x slower                                                     |
| sqlglot_optimize           | 51.7 ms                                                                | 68.7 ms: 1.33x slower                                                    |
| deepcopy_memo              | 29.7 us                                                                | 39.8 us: 1.34x slower                                                    |
| crypto_pyaes               | 68.0 ms                                                                | 91.2 ms: 1.34x slower                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 3.49 us: 1.34x slower                                                    |
| coverage                   | 78.1 ms                                                                | 105 ms: 1.35x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 448 ms: 1.35x slower                                                     |
| pprint_safe_repr           | 708 ms                                                                 | 955 ms: 1.35x slower                                                     |
| pylint                     | 278 ms                                                                 | 379 ms: 1.36x slower                                                     |
| xml_etree_process          | 57.8 ms                                                                | 78.9 ms: 1.37x slower                                                    |
| python_startup_no_site     | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| pprint_pformat             | 1.45 sec                                                               | 1.99 sec: 1.37x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.55 sec: 1.39x slower                                                   |
| async_tree_memoization_tg  | 305 ms                                                                 | 425 ms: 1.39x slower                                                     |
| generators                 | 26.6 ms                                                                | 37.7 ms: 1.41x slower                                                    |
| regex_compile              | 127 ms                                                                 | 181 ms: 1.43x slower                                                     |
| nbody                      | 89.4 ms                                                                | 129 ms: 1.44x slower                                                     |
| 2to3                       | 253 ms                                                                 | 367 ms: 1.45x slower                                                     |
| django_template            | 34.6 ms                                                                | 50.2 ms: 1.45x slower                                                    |
| subparsers                 | 21.5 ms                                                                | 31.5 ms: 1.47x slower                                                    |
| genshi_text                | 21.4 ms                                                                | 31.5 ms: 1.47x slower                                                    |
| float                      | 77.2 ms                                                                | 115 ms: 1.48x slower                                                     |
| sympy_integrate            | 19.6 ms                                                                | 29.4 ms: 1.50x slower                                                    |
| sqlalchemy_imperative      | 18.8 ms                                                                | 29.1 ms: 1.55x slower                                                    |
| mako                       | 11.4 ms                                                                | 17.8 ms: 1.56x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 331 us: 1.59x slower                                                     |
| pickle_pure_python         | 314 us                                                                 | 499 us: 1.59x slower                                                     |
| pyflate                    | 439 ms                                                                 | 699 ms: 1.59x slower                                                     |
| comprehensions             | 17.0 us                                                                | 27.1 us: 1.60x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 202 ms: 1.61x slower                                                     |
| thrift                     | 726 us                                                                 | 1.19 ms: 1.63x slower                                                    |
| hexiom                     | 5.78 ms                                                                | 9.74 ms: 1.69x slower                                                    |
| logging_silent             | 106 ns                                                                 | 180 ns: 1.70x slower                                                     |
| richards_super             | 51.3 ms                                                                | 88.4 ms: 1.72x slower                                                    |
| scimark_lu                 | 107 ms                                                                 | 186 ms: 1.73x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 2.72 ms: 1.73x slower                                                    |
| richards                   | 45.3 ms                                                                | 79.0 ms: 1.74x slower                                                    |
| sympy_str                  | 268 ms                                                                 | 474 ms: 1.77x slower                                                     |
| scimark_sor                | 131 ms                                                                 | 232 ms: 1.78x slower                                                     |
| logging_format             | 6.78 us                                                                | 12.1 us: 1.78x slower                                                    |
| logging_simple             | 5.95 us                                                                | 10.8 us: 1.82x slower                                                    |
| chaos                      | 57.5 ms                                                                | 105 ms: 1.83x slower                                                     |
| sqlglot_parse              | 1.26 ms                                                                | 2.35 ms: 1.87x slower                                                    |
| scimark_monte_carlo        | 63.7 ms                                                                | 120 ms: 1.88x slower                                                     |
| sympy_expand               | 451 ms                                                                 | 952 ms: 2.11x slower                                                     |
| raytrace                   | 259 ms                                                                 | 562 ms: 2.17x slower                                                     |
| sympy_sum                  | 151 ms                                                                 | 349 ms: 2.31x slower                                                     |
| go                         | 117 ms                                                                 | 269 ms: 2.31x slower                                                     |
| deltablue                  | 3.16 ms                                                                | 8.09 ms: 2.56x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.41 ms: 3.32x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.38x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20241211-3.14.0a2+-7e3de44-NOGIL/bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44.json: html5lib

- Geometric mean (including insignificant results): 1.270x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.19x