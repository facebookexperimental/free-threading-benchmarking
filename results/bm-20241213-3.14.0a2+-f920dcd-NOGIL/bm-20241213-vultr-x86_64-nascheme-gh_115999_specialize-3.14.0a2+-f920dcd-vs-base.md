# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: f920dcd
- commit date: 2024-12-13
- overall geometric mean: 1.026x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 366 ms: 1.00x faster                                                     |
| html5lib       | 97.9 ms                                                                | 95.5 ms: 1.03x faster                                                    |
| sphinx         | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 358 ms                                                                 | 328 ms: 1.09x faster                                                     |
| async_tree_io_tg           | 822 ms                                                                 | 763 ms: 1.08x faster                                                     |
| async_tree_memoization_tg  | 445 ms                                                                 | 416 ms: 1.07x faster                                                     |
| async_tree_none            | 388 ms                                                                 | 363 ms: 1.07x faster                                                     |
| async_tree_io              | 841 ms                                                                 | 788 ms: 1.07x faster                                                     |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 583 ms: 1.06x faster                                                     |
| async_tree_memoization     | 469 ms                                                                 | 444 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 612 ms: 1.05x faster                                                     |
| async_generators           | 456 ms                                                                 | 449 ms: 1.02x faster                                                     |
| coroutines                 | 24.9 ms                                                                | 24.5 ms: 1.02x faster                                                    |
| asyncio_websockets         | 521 ms                                                                 | 519 ms: 1.00x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 137 ms                                                                 | 115 ms: 1.19x faster                                                     |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                     |
| nbody          | 128 ms                                                                 | 130 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                 | 173 ms: 1.04x faster                                                     |
| regex_dna      | 182 ms                                                                 | 181 ms: 1.00x faster                                                     |
| regex_effbot   | 2.79 ms                                                                | 2.77 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 77.9 ms                                                                | 73.7 ms: 1.06x faster                                                    |
| tomli_loads          | 2.67 sec                                                               | 2.61 sec: 1.03x faster                                                   |
| pickle_pure_python   | 515 us                                                                 | 503 us: 1.02x faster                                                     |
| xml_etree_iterparse  | 91.3 ms                                                                | 90.0 ms: 1.01x faster                                                    |
| unpickle_pure_python | 333 us                                                                 | 329 us: 1.01x faster                                                     |
| xml_etree_parse      | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (3): json_loads, xml_etree_generate, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                    |
| mako            | 17.7 ms                                                                | 17.5 ms: 1.01x faster                                                    |
| genshi_text     | 31.9 ms                                                                | 31.6 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 137 ms                                                                 | 115 ms: 1.19x faster                                                     |
| richards                   | 76.7 ms                                                                | 67.8 ms: 1.13x faster                                                    |
| richards_super             | 86.2 ms                                                                | 76.2 ms: 1.13x faster                                                    |
| raytrace                   | 547 ms                                                                 | 498 ms: 1.10x faster                                                     |
| thrift                     | 1.16 ms                                                                | 1.06 ms: 1.10x faster                                                    |
| async_tree_none_tg         | 358 ms                                                                 | 328 ms: 1.09x faster                                                     |
| scimark_monte_carlo        | 118 ms                                                                 | 108 ms: 1.09x faster                                                     |
| pycparser                  | 1.55 sec                                                               | 1.42 sec: 1.09x faster                                                   |
| sqlglot_parse              | 2.58 ms                                                                | 2.37 ms: 1.09x faster                                                    |
| go                         | 267 ms                                                                 | 245 ms: 1.09x faster                                                     |
| async_tree_io_tg           | 822 ms                                                                 | 763 ms: 1.08x faster                                                     |
| sqlglot_transpile          | 2.93 ms                                                                | 2.74 ms: 1.07x faster                                                    |
| async_tree_memoization_tg  | 445 ms                                                                 | 416 ms: 1.07x faster                                                     |
| async_tree_none            | 388 ms                                                                 | 363 ms: 1.07x faster                                                     |
| deltablue                  | 8.00 ms                                                                | 7.49 ms: 1.07x faster                                                    |
| chaos                      | 104 ms                                                                 | 97.2 ms: 1.07x faster                                                    |
| async_tree_io              | 841 ms                                                                 | 788 ms: 1.07x faster                                                     |
| logging_format             | 12.0 us                                                                | 11.3 us: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 583 ms: 1.06x faster                                                     |
| xml_etree_process          | 77.9 ms                                                                | 73.7 ms: 1.06x faster                                                    |
| async_tree_memoization     | 469 ms                                                                 | 444 ms: 1.06x faster                                                     |
| sqlalchemy_imperative      | 29.8 ms                                                                | 28.3 ms: 1.05x faster                                                    |
| logging_simple             | 10.6 us                                                                | 10.1 us: 1.05x faster                                                    |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 612 ms: 1.05x faster                                                     |
| regex_compile              | 180 ms                                                                 | 173 ms: 1.04x faster                                                     |
| subparsers                 | 31.6 ms                                                                | 30.4 ms: 1.04x faster                                                    |
| dulwich_log                | 95.9 ms                                                                | 92.5 ms: 1.04x faster                                                    |
| pyflate                    | 699 ms                                                                 | 676 ms: 1.03x faster                                                     |
| html5lib                   | 97.9 ms                                                                | 95.5 ms: 1.03x faster                                                    |
| tomli_loads                | 2.67 sec                                                               | 2.61 sec: 1.03x faster                                                   |
| pickle_pure_python         | 515 us                                                                 | 503 us: 1.02x faster                                                     |
| pprint_pformat             | 2.02 sec                                                               | 1.98 sec: 1.02x faster                                                   |
| sqlite_synth               | 2.29 us                                                                | 2.25 us: 1.02x faster                                                    |
| sqlalchemy_declarative     | 203 ms                                                                 | 199 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.86 ms                                                                | 1.83 ms: 1.02x faster                                                    |
| telco                      | 8.84 ms                                                                | 8.69 ms: 1.02x faster                                                    |
| hexiom                     | 9.88 ms                                                                | 9.72 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 970 ms                                                                 | 955 ms: 1.02x faster                                                     |
| async_generators           | 456 ms                                                                 | 449 ms: 1.02x faster                                                     |
| coroutines                 | 24.9 ms                                                                | 24.5 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 6.04 ms                                                                | 5.95 ms: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 91.3 ms                                                                | 90.0 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 203 us                                                                 | 201 us: 1.01x faster                                                     |
| django_template            | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                    |
| mako                       | 17.7 ms                                                                | 17.5 ms: 1.01x faster                                                    |
| comprehensions             | 27.4 us                                                                | 27.2 us: 1.01x faster                                                    |
| unpickle_pure_python       | 333 us                                                                 | 329 us: 1.01x faster                                                     |
| genshi_text                | 31.9 ms                                                                | 31.6 ms: 1.01x faster                                                    |
| scimark_lu                 | 184 ms                                                                 | 183 ms: 1.01x faster                                                     |
| gc_traversal               | 3.54 ms                                                                | 3.51 ms: 1.01x faster                                                    |
| pathlib                    | 20.2 ms                                                                | 20.0 ms: 1.01x faster                                                    |
| xml_etree_parse            | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                     |
| deepcopy_reduce            | 3.49 us                                                                | 3.47 us: 1.01x faster                                                    |
| python_startup             | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                                    |
| sphinx                     | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| sympy_sum                  | 350 ms                                                                 | 348 ms: 1.01x faster                                                     |
| sympy_expand               | 955 ms                                                                 | 950 ms: 1.01x faster                                                     |
| regex_dna                  | 182 ms                                                                 | 181 ms: 1.00x faster                                                     |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                    |
| regex_effbot               | 2.79 ms                                                                | 2.77 ms: 1.00x faster                                                    |
| scimark_sor                | 236 ms                                                                 | 235 ms: 1.00x faster                                                     |
| many_optionals             | 1.29 ms                                                                | 1.28 ms: 1.00x faster                                                    |
| bpe_tokeniser              | 4.99 sec                                                               | 4.97 sec: 1.00x faster                                                   |
| asyncio_websockets         | 521 ms                                                                 | 519 ms: 1.00x faster                                                     |
| deepcopy_memo              | 39.6 us                                                                | 39.4 us: 1.00x faster                                                    |
| sympy_integrate            | 29.6 ms                                                                | 29.5 ms: 1.00x faster                                                    |
| 2to3                       | 367 ms                                                                 | 366 ms: 1.00x faster                                                     |
| crypto_pyaes               | 92.1 ms                                                                | 91.9 ms: 1.00x faster                                                    |
| mdp                        | 2.89 sec                                                               | 2.90 sec: 1.00x slower                                                   |
| k_core                     | 2.42 sec                                                               | 2.42 sec: 1.00x slower                                                   |
| sqlglot_normalize          | 133 ms                                                                 | 134 ms: 1.00x slower                                                     |
| fannkuch                   | 495 ms                                                                 | 498 ms: 1.00x slower                                                     |
| spectral_norm              | 123 ms                                                                 | 123 ms: 1.01x slower                                                     |
| nqueens                    | 97.4 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| generators                 | 38.0 ms                                                                | 38.3 ms: 1.01x slower                                                    |
| deepcopy                   | 324 us                                                                 | 327 us: 1.01x slower                                                     |
| scimark_fft                | 398 ms                                                                 | 401 ms: 1.01x slower                                                     |
| json                       | 5.02 ms                                                                | 5.07 ms: 1.01x slower                                                    |
| nbody                      | 128 ms                                                                 | 130 ms: 1.01x slower                                                     |
| coverage                   | 99.5 ms                                                                | 103 ms: 1.03x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (14): pylint, meteor_contest, json_loads, sympy_str, sqlglot_optimize, regex_v8, xml_etree_generate, logging_silent, docutils, genshi_xml, connected_components, shortest_path, json_dumps, bench_thread_pool

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x