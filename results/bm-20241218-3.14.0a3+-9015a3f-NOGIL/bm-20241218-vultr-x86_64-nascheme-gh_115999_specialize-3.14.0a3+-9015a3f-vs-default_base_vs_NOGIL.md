# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 9015a3f
- commit date: 2024-12-18
- overall geometric mean: 1.247x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 360 ms: 1.41x slower                                                     |
| docutils       | 2.54 sec                                                               | 3.03 sec: 1.19x slower                                                   |
| sphinx         | 987 ms                                                                 | 1.16 sec: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 581 ms                                                                 | 575 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 602 ms                                                                 | 598 ms: 1.01x faster                                                     |
| coroutines                 | 21.8 ms                                                                | 24.8 ms: 1.14x slower                                                    |
| async_tree_io_tg           | 609 ms                                                                 | 738 ms: 1.21x slower                                                     |
| async_tree_io              | 621 ms                                                                 | 762 ms: 1.23x slower                                                     |
| async_tree_none_tg         | 257 ms                                                                 | 322 ms: 1.26x slower                                                     |
| async_tree_memoization     | 336 ms                                                                 | 430 ms: 1.28x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 354 ms: 1.28x slower                                                     |
| async_generators           | 353 ms                                                                 | 453 ms: 1.28x slower                                                     |
| async_tree_memoization_tg  | 308 ms                                                                 | 401 ms: 1.30x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 181 ms: 1.23x faster                                                     |
| nbody          | 89.7 ms                                                                | 129 ms: 1.44x slower                                                     |
| float          | 75.9 ms                                                                | 114 ms: 1.50x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.21x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| regex_dna      | 173 ms                                                                 | 184 ms: 1.06x slower                                                     |
| regex_compile  | 126 ms                                                                 | 169 ms: 1.34x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                     |
| json_loads           | 26.3 us                                                                | 28.5 us: 1.08x slower                                                    |
| xml_etree_generate   | 84.1 ms                                                                | 97.6 ms: 1.16x slower                                                    |
| json_dumps           | 11.4 ms                                                                | 14.1 ms: 1.24x slower                                                    |
| xml_etree_process    | 58.7 ms                                                                | 75.4 ms: 1.28x slower                                                    |
| tomli_loads          | 1.97 sec                                                               | 2.55 sec: 1.29x slower                                                   |
| unpickle_pure_python | 211 us                                                                 | 329 us: 1.56x slower                                                     |
| pickle_pure_python   | 313 us                                                                 | 506 us: 1.62x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 17.2 ms: 1.17x slower                                                    |
| python_startup_no_site | 7.50 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.8 ms                                                                | 63.4 ms: 1.27x slower                                                    |
| django_template | 35.1 ms                                                                | 49.1 ms: 1.40x slower                                                    |
| genshi_text     | 21.6 ms                                                                | 30.6 ms: 1.42x slower                                                    |
| mako            | 11.7 ms                                                                | 17.1 ms: 1.47x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.39x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 222 ms                                                                 | 181 ms: 1.23x faster                                                     |
| gc_traversal               | 4.20 ms                                                                | 3.51 ms: 1.20x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.14 us: 1.05x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 581 ms                                                                 | 575 ms: 1.01x faster                                                     |
| regex_effbot               | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 602 ms                                                                 | 598 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 90.6 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.01x slower                                                     |
| json                       | 4.78 ms                                                                | 5.05 ms: 1.06x slower                                                    |
| regex_dna                  | 173 ms                                                                 | 184 ms: 1.06x slower                                                     |
| pathlib                    | 18.3 ms                                                                | 19.6 ms: 1.07x slower                                                    |
| json_loads                 | 26.3 us                                                                | 28.5 us: 1.08x slower                                                    |
| spectral_norm              | 98.0 ms                                                                | 112 ms: 1.14x slower                                                     |
| coroutines                 | 21.8 ms                                                                | 24.8 ms: 1.14x slower                                                    |
| k_core                     | 2.05 sec                                                               | 2.35 sec: 1.15x slower                                                   |
| xml_etree_generate         | 84.1 ms                                                                | 97.6 ms: 1.16x slower                                                    |
| python_startup             | 14.7 ms                                                                | 17.2 ms: 1.17x slower                                                    |
| sphinx                     | 987 ms                                                                 | 1.16 sec: 1.18x slower                                                   |
| bpe_tokeniser              | 4.25 sec                                                               | 5.01 sec: 1.18x slower                                                   |
| docutils                   | 2.54 sec                                                               | 3.03 sec: 1.19x slower                                                   |
| many_optionals             | 1.03 ms                                                                | 1.23 ms: 1.19x slower                                                    |
| telco                      | 7.15 ms                                                                | 8.58 ms: 1.20x slower                                                    |
| dulwich_log                | 75.3 ms                                                                | 90.4 ms: 1.20x slower                                                    |
| bench_mp_pool              | 89.3 ms                                                                | 108 ms: 1.21x slower                                                     |
| mdp                        | 2.32 sec                                                               | 2.80 sec: 1.21x slower                                                   |
| async_tree_io_tg           | 609 ms                                                                 | 738 ms: 1.21x slower                                                     |
| async_tree_io              | 621 ms                                                                 | 762 ms: 1.23x slower                                                     |
| scimark_fft                | 309 ms                                                                 | 383 ms: 1.24x slower                                                     |
| json_dumps                 | 11.4 ms                                                                | 14.1 ms: 1.24x slower                                                    |
| connected_components       | 399 ms                                                                 | 496 ms: 1.24x slower                                                     |
| pycparser                  | 1.11 sec                                                               | 1.39 sec: 1.25x slower                                                   |
| async_tree_none_tg         | 257 ms                                                                 | 322 ms: 1.26x slower                                                     |
| shortest_path              | 439 ms                                                                 | 555 ms: 1.26x slower                                                     |
| sqlglot_optimize           | 51.9 ms                                                                | 65.8 ms: 1.27x slower                                                    |
| deepcopy                   | 253 us                                                                 | 321 us: 1.27x slower                                                     |
| coverage                   | 79.3 ms                                                                | 101 ms: 1.27x slower                                                     |
| nqueens                    | 77.1 ms                                                                | 98.2 ms: 1.27x slower                                                    |
| genshi_xml                 | 49.8 ms                                                                | 63.4 ms: 1.27x slower                                                    |
| async_tree_memoization     | 336 ms                                                                 | 430 ms: 1.28x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 354 ms: 1.28x slower                                                     |
| async_generators           | 353 ms                                                                 | 453 ms: 1.28x slower                                                     |
| xml_etree_process          | 58.7 ms                                                                | 75.4 ms: 1.28x slower                                                    |
| tomli_loads                | 1.97 sec                                                               | 2.55 sec: 1.29x slower                                                   |
| sqlglot_normalize          | 103 ms                                                                 | 133 ms: 1.29x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 130 ms: 1.30x slower                                                     |
| async_tree_memoization_tg  | 308 ms                                                                 | 401 ms: 1.30x slower                                                     |
| pylint                     | 279 ms                                                                 | 363 ms: 1.30x slower                                                     |
| deepcopy_reduce            | 2.58 us                                                                | 3.38 us: 1.31x slower                                                    |
| subparsers                 | 21.7 ms                                                                | 28.6 ms: 1.32x slower                                                    |
| thrift                     | 736 us                                                                 | 977 us: 1.33x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 207 us: 1.33x slower                                                     |
| fannkuch                   | 371 ms                                                                 | 495 ms: 1.33x slower                                                     |
| regex_compile              | 126 ms                                                                 | 169 ms: 1.34x slower                                                     |
| crypto_pyaes               | 67.3 ms                                                                | 90.4 ms: 1.34x slower                                                    |
| pprint_safe_repr           | 702 ms                                                                 | 954 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.50 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| deepcopy_memo              | 29.6 us                                                                | 40.5 us: 1.37x slower                                                    |
| pprint_pformat             | 1.45 sec                                                               | 1.99 sec: 1.38x slower                                                   |
| scimark_sparse_mat_mult    | 4.18 ms                                                                | 5.80 ms: 1.39x slower                                                    |
| django_template            | 35.1 ms                                                                | 49.1 ms: 1.40x slower                                                    |
| generators                 | 27.0 ms                                                                | 38.2 ms: 1.41x slower                                                    |
| 2to3                       | 255 ms                                                                 | 360 ms: 1.41x slower                                                     |
| genshi_text                | 21.6 ms                                                                | 30.6 ms: 1.42x slower                                                    |
| nbody                      | 89.7 ms                                                                | 129 ms: 1.44x slower                                                     |
| sqlalchemy_imperative      | 18.9 ms                                                                | 27.6 ms: 1.46x slower                                                    |
| mako                       | 11.7 ms                                                                | 17.1 ms: 1.47x slower                                                    |
| logging_format             | 6.79 us                                                                | 10.1 us: 1.49x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 29.4 ms: 1.49x slower                                                    |
| float                      | 75.9 ms                                                                | 114 ms: 1.50x slower                                                     |
| logging_simple             | 6.04 us                                                                | 9.11 us: 1.51x slower                                                    |
| richards_super             | 50.3 ms                                                                | 76.7 ms: 1.52x slower                                                    |
| richards                   | 44.4 ms                                                                | 68.5 ms: 1.54x slower                                                    |
| unpickle_pure_python       | 211 us                                                                 | 329 us: 1.56x slower                                                     |
| sqlalchemy_declarative     | 125 ms                                                                 | 196 ms: 1.56x slower                                                     |
| pyflate                    | 424 ms                                                                 | 663 ms: 1.56x slower                                                     |
| pickle_pure_python         | 313 us                                                                 | 506 us: 1.62x slower                                                     |
| comprehensions             | 16.9 us                                                                | 27.7 us: 1.64x slower                                                    |
| scimark_lu                 | 111 ms                                                                 | 183 ms: 1.65x slower                                                     |
| chaos                      | 57.5 ms                                                                | 95.4 ms: 1.66x slower                                                    |
| hexiom                     | 5.80 ms                                                                | 9.82 ms: 1.69x slower                                                    |
| scimark_monte_carlo        | 62.9 ms                                                                | 108 ms: 1.71x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                                | 2.73 ms: 1.74x slower                                                    |
| sympy_str                  | 270 ms                                                                 | 474 ms: 1.76x slower                                                     |
| logging_silent             | 104 ns                                                                 | 188 ns: 1.80x slower                                                     |
| scimark_sor                | 123 ms                                                                 | 232 ms: 1.88x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                                | 2.37 ms: 1.89x slower                                                    |
| raytrace                   | 256 ms                                                                 | 496 ms: 1.94x slower                                                     |
| sympy_expand               | 455 ms                                                                 | 953 ms: 2.09x slower                                                     |
| go                         | 115 ms                                                                 | 245 ms: 2.12x slower                                                     |
| sympy_sum                  | 153 ms                                                                 | 348 ms: 2.28x slower                                                     |
| deltablue                  | 3.15 ms                                                                | 7.66 ms: 2.43x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.39 ms: 3.29x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.34x slower                                                             |

Benchmark hidden because not significant (2): regex_v8, create_gc_cycles
Ignored benchmarks (1) of results/bm-20241218-3.14.0a3+-9015a3f-NOGIL/bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f.json: html5lib

- Geometric mean (including insignificant results): 1.247x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x