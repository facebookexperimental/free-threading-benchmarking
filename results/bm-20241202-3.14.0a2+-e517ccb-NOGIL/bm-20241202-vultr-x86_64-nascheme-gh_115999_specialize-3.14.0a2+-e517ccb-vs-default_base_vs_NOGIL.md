# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.279x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 382 ms: 1.48x slower                                                     |
| docutils       | 2.61 sec                                                               | 3.22 sec: 1.23x slower                                                   |
| sphinx         | 1.02 sec                                                               | 1.24 sec: 1.21x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.30x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 667 ms                                                                 | 634 ms: 1.05x faster                                                     |
| async_tree_io_tg           | 887 ms                                                                 | 871 ms: 1.02x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_io              | 867 ms                                                                 | 898 ms: 1.04x slower                                                     |
| async_tree_none_tg         | 348 ms                                                                 | 372 ms: 1.07x slower                                                     |
| async_tree_memoization_tg  | 392 ms                                                                 | 464 ms: 1.18x slower                                                     |
| async_tree_memoization     | 413 ms                                                                 | 495 ms: 1.20x slower                                                     |
| async_tree_none            | 335 ms                                                                 | 403 ms: 1.20x slower                                                     |
| coroutines                 | 22.6 ms                                                                | 28.5 ms: 1.26x slower                                                    |
| async_generators           | 373 ms                                                                 | 474 ms: 1.27x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                             |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 184 ms: 1.21x faster                                                     |
| nbody          | 94.4 ms                                                                | 147 ms: 1.55x slower                                                     |
| float          | 81.3 ms                                                                | 143 ms: 1.76x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.31x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 185 ms: 1.06x slower                                                     |
| regex_v8       | 24.5 ms                                                                | 26.3 ms: 1.07x slower                                                    |
| regex_effbot   | 2.62 ms                                                                | 2.97 ms: 1.13x slower                                                    |
| regex_compile  | 130 ms                                                                 | 195 ms: 1.50x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 137 ms                                                                 | 132 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 98.3 ms                                                                | 95.6 ms: 1.03x faster                                                    |
| json_loads           | 24.9 us                                                                | 27.9 us: 1.12x slower                                                    |
| xml_etree_generate   | 86.2 ms                                                                | 103 ms: 1.20x slower                                                     |
| json_dumps           | 11.4 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| xml_etree_process    | 60.8 ms                                                                | 83.6 ms: 1.37x slower                                                    |
| tomli_loads          | 2.11 sec                                                               | 2.92 sec: 1.39x slower                                                   |
| unpickle_pure_python | 216 us                                                                 | 374 us: 1.73x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 560 us: 1.74x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.6 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.40 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.8 ms                                                                | 68.1 ms: 1.34x slower                                                    |
| genshi_text     | 22.7 ms                                                                | 34.6 ms: 1.53x slower                                                    |
| django_template | 35.8 ms                                                                | 55.4 ms: 1.55x slower                                                    |
| mako            | 11.6 ms                                                                | 20.2 ms: 1.74x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.53x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 222 ms                                                                 | 184 ms: 1.21x faster                                                     |
| gc_traversal               | 3.95 ms                                                                | 3.53 ms: 1.12x faster                                                    |
| create_gc_cycles           | 1.96 ms                                                                | 1.86 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg | 667 ms                                                                 | 634 ms: 1.05x faster                                                     |
| xml_etree_parse            | 137 ms                                                                 | 132 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 98.3 ms                                                                | 95.6 ms: 1.03x faster                                                    |
| async_tree_io_tg           | 887 ms                                                                 | 871 ms: 1.02x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                     |
| async_tree_io              | 867 ms                                                                 | 898 ms: 1.04x slower                                                     |
| sqlite_synth               | 2.21 us                                                                | 2.34 us: 1.05x slower                                                    |
| regex_dna                  | 175 ms                                                                 | 185 ms: 1.06x slower                                                     |
| async_tree_none_tg         | 348 ms                                                                 | 372 ms: 1.07x slower                                                     |
| regex_v8                   | 24.5 ms                                                                | 26.3 ms: 1.07x slower                                                    |
| json                       | 4.57 ms                                                                | 5.05 ms: 1.11x slower                                                    |
| json_loads                 | 24.9 us                                                                | 27.9 us: 1.12x slower                                                    |
| spectral_norm              | 115 ms                                                                 | 130 ms: 1.13x slower                                                     |
| regex_effbot               | 2.62 ms                                                                | 2.97 ms: 1.13x slower                                                    |
| pathlib                    | 18.4 ms                                                                | 20.8 ms: 1.13x slower                                                    |
| scimark_fft                | 339 ms                                                                 | 389 ms: 1.15x slower                                                     |
| async_tree_memoization_tg  | 392 ms                                                                 | 464 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult    | 4.55 ms                                                                | 5.39 ms: 1.18x slower                                                    |
| xml_etree_generate         | 86.2 ms                                                                | 103 ms: 1.20x slower                                                     |
| async_tree_memoization     | 413 ms                                                                 | 495 ms: 1.20x slower                                                     |
| async_tree_none            | 335 ms                                                                 | 403 ms: 1.20x slower                                                     |
| python_startup             | 14.6 ms                                                                | 17.6 ms: 1.20x slower                                                    |
| sphinx                     | 1.02 sec                                                               | 1.24 sec: 1.21x slower                                                   |
| telco                      | 7.31 ms                                                                | 9.01 ms: 1.23x slower                                                    |
| docutils                   | 2.61 sec                                                               | 3.22 sec: 1.23x slower                                                   |
| mdp                        | 2.48 sec                                                               | 3.07 sec: 1.24x slower                                                   |
| bpe_tokeniser              | 4.44 sec                                                               | 5.58 sec: 1.26x slower                                                   |
| coroutines                 | 22.6 ms                                                                | 28.5 ms: 1.26x slower                                                    |
| json_dumps                 | 11.4 ms                                                                | 14.4 ms: 1.27x slower                                                    |
| async_generators           | 373 ms                                                                 | 474 ms: 1.27x slower                                                     |
| coverage                   | 79.3 ms                                                                | 101 ms: 1.27x slower                                                     |
| shortest_path              | 443 ms                                                                 | 564 ms: 1.27x slower                                                     |
| connected_components       | 401 ms                                                                 | 513 ms: 1.28x slower                                                     |
| bench_mp_pool              | 86.3 ms                                                                | 110 ms: 1.28x slower                                                     |
| dulwich_log                | 76.2 ms                                                                | 99.5 ms: 1.31x slower                                                    |
| nqueens                    | 80.9 ms                                                                | 107 ms: 1.32x slower                                                     |
| genshi_xml                 | 50.8 ms                                                                | 68.1 ms: 1.34x slower                                                    |
| generators                 | 29.4 ms                                                                | 39.5 ms: 1.34x slower                                                    |
| many_optionals             | 1.02 ms                                                                | 1.37 ms: 1.34x slower                                                    |
| deepcopy                   | 265 us                                                                 | 357 us: 1.35x slower                                                     |
| meteor_contest             | 100.0 ms                                                               | 137 ms: 1.37x slower                                                     |
| xml_etree_process          | 60.8 ms                                                                | 83.6 ms: 1.37x slower                                                    |
| typing_runtime_protocols   | 158 us                                                                 | 218 us: 1.38x slower                                                     |
| tomli_loads                | 2.11 sec                                                               | 2.92 sec: 1.39x slower                                                   |
| sqlglot_optimize           | 54.1 ms                                                                | 75.2 ms: 1.39x slower                                                    |
| python_startup_no_site     | 7.40 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| sqlglot_normalize          | 108 ms                                                                 | 151 ms: 1.40x slower                                                     |
| fannkuch                   | 381 ms                                                                 | 535 ms: 1.41x slower                                                     |
| pycparser                  | 1.14 sec                                                               | 1.61 sec: 1.41x slower                                                   |
| deepcopy_reduce            | 2.63 us                                                                | 3.73 us: 1.42x slower                                                    |
| pylint                     | 270 ms                                                                 | 396 ms: 1.46x slower                                                     |
| deepcopy_memo              | 30.5 us                                                                | 44.7 us: 1.47x slower                                                    |
| pprint_safe_repr           | 733 ms                                                                 | 1.08 sec: 1.47x slower                                                   |
| 2to3                       | 258 ms                                                                 | 382 ms: 1.48x slower                                                     |
| regex_compile              | 130 ms                                                                 | 195 ms: 1.50x slower                                                     |
| pprint_pformat             | 1.48 sec                                                               | 2.23 sec: 1.51x slower                                                   |
| subparsers                 | 22.0 ms                                                                | 33.2 ms: 1.51x slower                                                    |
| crypto_pyaes               | 67.4 ms                                                                | 102 ms: 1.51x slower                                                     |
| genshi_text                | 22.7 ms                                                                | 34.6 ms: 1.53x slower                                                    |
| django_template            | 35.8 ms                                                                | 55.4 ms: 1.55x slower                                                    |
| sympy_integrate            | 20.0 ms                                                                | 31.0 ms: 1.55x slower                                                    |
| nbody                      | 94.4 ms                                                                | 147 ms: 1.55x slower                                                     |
| pyflate                    | 450 ms                                                                 | 728 ms: 1.62x slower                                                     |
| thrift                     | 743 us                                                                 | 1.21 ms: 1.62x slower                                                    |
| comprehensions             | 17.8 us                                                                | 29.2 us: 1.64x slower                                                    |
| unpickle_pure_python       | 216 us                                                                 | 374 us: 1.73x slower                                                     |
| logging_silent             | 112 ns                                                                 | 194 ns: 1.73x slower                                                     |
| scimark_lu                 | 114 ms                                                                 | 199 ms: 1.73x slower                                                     |
| pickle_pure_python         | 321 us                                                                 | 560 us: 1.74x slower                                                     |
| mako                       | 11.6 ms                                                                | 20.2 ms: 1.74x slower                                                    |
| float                      | 81.3 ms                                                                | 143 ms: 1.76x slower                                                     |
| scimark_sor                | 137 ms                                                                 | 241 ms: 1.77x slower                                                     |
| logging_format             | 7.08 us                                                                | 12.8 us: 1.81x slower                                                    |
| sympy_str                  | 275 ms                                                                 | 497 ms: 1.81x slower                                                     |
| richards                   | 47.4 ms                                                                | 86.4 ms: 1.82x slower                                                    |
| logging_simple             | 6.20 us                                                                | 11.5 us: 1.85x slower                                                    |
| hexiom                     | 6.03 ms                                                                | 11.3 ms: 1.87x slower                                                    |
| scimark_monte_carlo        | 65.3 ms                                                                | 123 ms: 1.88x slower                                                     |
| richards_super             | 53.6 ms                                                                | 102 ms: 1.91x slower                                                     |
| sqlglot_transpile          | 1.61 ms                                                                | 3.10 ms: 1.93x slower                                                    |
| chaos                      | 58.9 ms                                                                | 115 ms: 1.94x slower                                                     |
| sqlglot_parse              | 1.31 ms                                                                | 2.70 ms: 2.06x slower                                                    |
| sympy_expand               | 466 ms                                                                 | 992 ms: 2.13x slower                                                     |
| raytrace                   | 269 ms                                                                 | 607 ms: 2.26x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 358 ms: 2.32x slower                                                     |
| go                         | 121 ms                                                                 | 284 ms: 2.34x slower                                                     |
| deltablue                  | 3.29 ms                                                                | 8.79 ms: 2.67x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.39 ms: 3.31x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.40x slower                                                             |

Benchmark hidden because not significant (2): k_core, async_tree_cpu_io_mixed
Ignored benchmarks (2) of results/bm-20241129-3.14.0a2+-15d6506/bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241202-3.14.0a2+-e517ccb-NOGIL/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb.json: html5lib

- Geometric mean (including insignificant results): 1.279x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x