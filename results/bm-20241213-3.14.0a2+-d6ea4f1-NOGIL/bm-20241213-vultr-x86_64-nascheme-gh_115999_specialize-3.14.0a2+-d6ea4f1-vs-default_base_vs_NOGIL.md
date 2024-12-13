# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.252x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 365 ms: 1.44x slower                                                     |
| docutils       | 2.53 sec                                                               | 3.07 sec: 1.22x slower                                                   |
| sphinx         | 980 ms                                                                 | 1.18 sec: 1.21x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 593 ms: 1.08x slower                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 620 ms: 1.09x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 24.1 ms: 1.13x slower                                                    |
| async_generators           | 359 ms                                                                 | 438 ms: 1.22x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 765 ms: 1.25x slower                                                     |
| async_tree_io              | 625 ms                                                                 | 793 ms: 1.27x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 329 ms: 1.29x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 362 ms: 1.31x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 446 ms: 1.34x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 420 ms: 1.37x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.21x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                     |
| nbody          | 89.4 ms                                                                | 126 ms: 1.41x slower                                                     |
| float          | 77.2 ms                                                                | 113 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.21x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 24.1 ms: 1.02x faster                                                    |
| regex_effbot   | 2.68 ms                                                                | 2.80 ms: 1.04x slower                                                    |
| regex_dna      | 172 ms                                                                 | 183 ms: 1.07x slower                                                     |
| regex_compile  | 127 ms                                                                 | 172 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| json_loads           | 26.5 us                                                                | 28.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 82.9 ms                                                                | 96.5 ms: 1.16x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.1 ms: 1.24x slower                                                    |
| tomli_loads          | 2.06 sec                                                               | 2.60 sec: 1.26x slower                                                   |
| xml_etree_process    | 57.8 ms                                                                | 73.1 ms: 1.27x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 326 us: 1.57x slower                                                     |
| pickle_pure_python   | 314 us                                                                 | 492 us: 1.57x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                    |
| python_startup_no_site | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 62.9 ms: 1.27x slower                                                    |
| genshi_text     | 21.4 ms                                                                | 31.2 ms: 1.46x slower                                                    |
| django_template | 34.6 ms                                                                | 50.5 ms: 1.46x slower                                                    |
| mako            | 11.4 ms                                                                | 17.6 ms: 1.54x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.43x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.62 ms                                                                | 3.52 ms: 1.31x faster                                                    |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                     |
| sqlite_synth               | 2.23 us                                                                | 2.18 us: 1.02x faster                                                    |
| regex_v8                   | 24.5 ms                                                                | 24.1 ms: 1.02x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                     |
| xml_etree_parse            | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| regex_effbot               | 2.68 ms                                                                | 2.80 ms: 1.04x slower                                                    |
| json                       | 4.81 ms                                                                | 5.05 ms: 1.05x slower                                                    |
| regex_dna                  | 172 ms                                                                 | 183 ms: 1.07x slower                                                     |
| json_loads                 | 26.5 us                                                                | 28.6 us: 1.08x slower                                                    |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 593 ms: 1.08x slower                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 620 ms: 1.09x slower                                                     |
| pathlib                    | 18.4 ms                                                                | 20.1 ms: 1.10x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 120 ms: 1.12x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 24.1 ms: 1.13x slower                                                    |
| xml_etree_generate         | 82.9 ms                                                                | 96.5 ms: 1.16x slower                                                    |
| bpe_tokeniser              | 4.23 sec                                                               | 4.93 sec: 1.17x slower                                                   |
| k_core                     | 2.06 sec                                                               | 2.41 sec: 1.17x slower                                                   |
| scimark_fft                | 323 ms                                                                 | 384 ms: 1.19x slower                                                     |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                    |
| telco                      | 7.26 ms                                                                | 8.70 ms: 1.20x slower                                                    |
| sphinx                     | 980 ms                                                                 | 1.18 sec: 1.21x slower                                                   |
| docutils                   | 2.53 sec                                                               | 3.07 sec: 1.22x slower                                                   |
| bench_mp_pool              | 88.9 ms                                                                | 108 ms: 1.22x slower                                                     |
| async_generators           | 359 ms                                                                 | 438 ms: 1.22x slower                                                     |
| nqueens                    | 78.8 ms                                                                | 96.8 ms: 1.23x slower                                                    |
| mdp                        | 2.34 sec                                                               | 2.89 sec: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.39 ms: 1.23x slower                                                    |
| dulwich_log                | 74.8 ms                                                                | 92.9 ms: 1.24x slower                                                    |
| json_dumps                 | 11.3 ms                                                                | 14.1 ms: 1.24x slower                                                    |
| shortest_path              | 439 ms                                                                 | 549 ms: 1.25x slower                                                     |
| connected_components       | 398 ms                                                                 | 499 ms: 1.25x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 765 ms: 1.25x slower                                                     |
| tomli_loads                | 2.06 sec                                                               | 2.60 sec: 1.26x slower                                                   |
| xml_etree_process          | 57.8 ms                                                                | 73.1 ms: 1.27x slower                                                    |
| async_tree_io              | 625 ms                                                                 | 793 ms: 1.27x slower                                                     |
| genshi_xml                 | 49.3 ms                                                                | 62.9 ms: 1.27x slower                                                    |
| many_optionals             | 1.01 ms                                                                | 1.29 ms: 1.27x slower                                                    |
| deepcopy                   | 252 us                                                                 | 323 us: 1.28x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.43 sec: 1.28x slower                                                   |
| typing_runtime_protocols   | 154 us                                                                 | 199 us: 1.29x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 329 ms: 1.29x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 133 ms: 1.30x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 130 ms: 1.30x slower                                                     |
| deepcopy_memo              | 29.7 us                                                                | 38.8 us: 1.31x slower                                                    |
| async_tree_none            | 277 ms                                                                 | 362 ms: 1.31x slower                                                     |
| fannkuch                   | 375 ms                                                                 | 492 ms: 1.31x slower                                                     |
| sqlglot_optimize           | 51.7 ms                                                                | 68.3 ms: 1.32x slower                                                    |
| crypto_pyaes               | 68.0 ms                                                                | 90.0 ms: 1.32x slower                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 3.45 us: 1.33x slower                                                    |
| coverage                   | 78.1 ms                                                                | 104 ms: 1.33x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 446 ms: 1.34x slower                                                     |
| pylint                     | 278 ms                                                                 | 376 ms: 1.35x slower                                                     |
| regex_compile              | 127 ms                                                                 | 172 ms: 1.35x slower                                                     |
| pprint_safe_repr           | 708 ms                                                                 | 962 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 420 ms: 1.37x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 2.00 sec: 1.38x slower                                                   |
| nbody                      | 89.4 ms                                                                | 126 ms: 1.41x slower                                                     |
| subparsers                 | 21.5 ms                                                                | 30.3 ms: 1.41x slower                                                    |
| generators                 | 26.6 ms                                                                | 37.6 ms: 1.41x slower                                                    |
| thrift                     | 726 us                                                                 | 1.03 ms: 1.42x slower                                                    |
| 2to3                       | 253 ms                                                                 | 365 ms: 1.44x slower                                                     |
| genshi_text                | 21.4 ms                                                                | 31.2 ms: 1.46x slower                                                    |
| django_template            | 34.6 ms                                                                | 50.5 ms: 1.46x slower                                                    |
| float                      | 77.2 ms                                                                | 113 ms: 1.47x slower                                                     |
| richards_super             | 51.3 ms                                                                | 75.4 ms: 1.47x slower                                                    |
| richards                   | 45.3 ms                                                                | 66.8 ms: 1.47x slower                                                    |
| sympy_integrate            | 19.6 ms                                                                | 29.5 ms: 1.50x slower                                                    |
| sqlalchemy_imperative      | 18.8 ms                                                                | 28.5 ms: 1.51x slower                                                    |
| pyflate                    | 439 ms                                                                 | 673 ms: 1.53x slower                                                     |
| mako                       | 11.4 ms                                                                | 17.6 ms: 1.54x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 326 us: 1.57x slower                                                     |
| pickle_pure_python         | 314 us                                                                 | 492 us: 1.57x slower                                                     |
| comprehensions             | 17.0 us                                                                | 26.8 us: 1.58x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 199 ms: 1.58x slower                                                     |
| logging_format             | 6.78 us                                                                | 11.1 us: 1.64x slower                                                    |
| scimark_monte_carlo        | 63.7 ms                                                                | 105 ms: 1.64x slower                                                     |
| chaos                      | 57.5 ms                                                                | 95.0 ms: 1.65x slower                                                    |
| hexiom                     | 5.78 ms                                                                | 9.63 ms: 1.67x slower                                                    |
| scimark_lu                 | 107 ms                                                                 | 180 ms: 1.67x slower                                                     |
| logging_simple             | 5.95 us                                                                | 9.97 us: 1.68x slower                                                    |
| logging_silent             | 106 ns                                                                 | 180 ns: 1.69x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 2.69 ms: 1.72x slower                                                    |
| scimark_sor                | 131 ms                                                                 | 230 ms: 1.76x slower                                                     |
| sympy_str                  | 268 ms                                                                 | 474 ms: 1.77x slower                                                     |
| sqlglot_parse              | 1.26 ms                                                                | 2.33 ms: 1.85x slower                                                    |
| raytrace                   | 259 ms                                                                 | 489 ms: 1.89x slower                                                     |
| go                         | 117 ms                                                                 | 241 ms: 2.07x slower                                                     |
| sympy_expand               | 451 ms                                                                 | 952 ms: 2.11x slower                                                     |
| sympy_sum                  | 151 ms                                                                 | 348 ms: 2.30x slower                                                     |
| deltablue                  | 3.16 ms                                                                | 7.35 ms: 2.33x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.41 ms: 3.32x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.35x slower                                                             |

Benchmark hidden because not significant (2): create_gc_cycles, xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1.json: html5lib

- Geometric mean (including insignificant results): 1.252x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x