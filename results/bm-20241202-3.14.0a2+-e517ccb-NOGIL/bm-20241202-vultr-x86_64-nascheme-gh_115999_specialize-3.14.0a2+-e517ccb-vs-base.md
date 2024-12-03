# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 379 ms                                                                 | 382 ms: 1.01x slower                                                     |
| html5lib       | 101 ms                                                                 | 101 ms: 1.01x faster                                                     |
| sphinx         | 1.23 sec                                                               | 1.24 sec: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 895 ms                                                                 | 898 ms: 1.00x slower                                                     |
| async_tree_memoization     | 493 ms                                                                 | 495 ms: 1.00x slower                                                     |
| async_tree_none            | 401 ms                                                                 | 403 ms: 1.01x slower                                                     |
| async_tree_io_tg           | 866 ms                                                                 | 871 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 368 ms                                                                 | 372 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 627 ms                                                                 | 634 ms: 1.01x slower                                                     |
| async_generators           | 468 ms                                                                 | 474 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 659 ms                                                                 | 668 ms: 1.01x slower                                                     |
| coroutines                 | 27.9 ms                                                                | 28.5 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 142 ms                                                                 | 143 ms: 1.01x slower                                                     |
| pidigits       | 181 ms                                                                 | 184 ms: 1.01x slower                                                     |
| nbody          | 142 ms                                                                 | 147 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 184 ms                                                                 | 185 ms: 1.00x slower                                                     |
| regex_effbot   | 2.85 ms                                                                | 2.97 ms: 1.04x slower                                                    |
| regex_v8       | 25.2 ms                                                                | 26.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 28.1 us                                                                | 27.9 us: 1.01x faster                                                    |
| unpickle_pure_python | 376 us                                                                 | 374 us: 1.00x faster                                                     |
| xml_etree_parse      | 131 ms                                                                 | 132 ms: 1.01x slower                                                     |
| tomli_loads          | 2.91 sec                                                               | 2.92 sec: 1.01x slower                                                   |
| xml_etree_iterparse  | 94.9 ms                                                                | 95.6 ms: 1.01x slower                                                    |
| xml_etree_process    | 82.6 ms                                                                | 83.6 ms: 1.01x slower                                                    |
| pickle_pure_python   | 552 us                                                                 | 560 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.6 ms: 1.01x slower                                                    |
| python_startup_no_site | 10.2 ms                                                                | 10.3 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 55.8 ms                                                                | 55.4 ms: 1.01x faster                                                    |
| genshi_xml      | 67.5 ms                                                                | 68.1 ms: 1.01x slower                                                    |
| genshi_text     | 34.3 ms                                                                | 34.6 ms: 1.01x slower                                                    |
| mako            | 19.7 ms                                                                | 20.2 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 5.67 ms                                                                | 5.39 ms: 1.05x faster                                                    |
| logging_silent             | 200 ns                                                                 | 194 ns: 1.03x faster                                                     |
| scimark_lu                 | 203 ms                                                                 | 199 ms: 1.02x faster                                                     |
| scimark_fft                | 396 ms                                                                 | 389 ms: 1.02x faster                                                     |
| scimark_sor                | 245 ms                                                                 | 241 ms: 1.01x faster                                                     |
| hexiom                     | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                                    |
| fannkuch                   | 541 ms                                                                 | 535 ms: 1.01x faster                                                     |
| deepcopy_memo              | 45.2 us                                                                | 44.7 us: 1.01x faster                                                    |
| bpe_tokeniser              | 5.64 sec                                                               | 5.58 sec: 1.01x faster                                                   |
| django_template            | 55.8 ms                                                                | 55.4 ms: 1.01x faster                                                    |
| json_loads                 | 28.1 us                                                                | 27.9 us: 1.01x faster                                                    |
| html5lib                   | 101 ms                                                                 | 101 ms: 1.01x faster                                                     |
| raytrace                   | 611 ms                                                                 | 607 ms: 1.01x faster                                                     |
| pyflate                    | 732 ms                                                                 | 728 ms: 1.01x faster                                                     |
| nqueens                    | 107 ms                                                                 | 107 ms: 1.00x faster                                                     |
| unpickle_pure_python       | 376 us                                                                 | 374 us: 1.00x faster                                                     |
| pycparser                  | 1.61 sec                                                               | 1.61 sec: 1.00x faster                                                   |
| crypto_pyaes               | 102 ms                                                                 | 102 ms: 1.00x faster                                                     |
| async_tree_io              | 895 ms                                                                 | 898 ms: 1.00x slower                                                     |
| sympy_str                  | 495 ms                                                                 | 497 ms: 1.00x slower                                                     |
| spectral_norm              | 129 ms                                                                 | 130 ms: 1.00x slower                                                     |
| regex_dna                  | 184 ms                                                                 | 185 ms: 1.00x slower                                                     |
| shortest_path              | 561 ms                                                                 | 564 ms: 1.00x slower                                                     |
| async_tree_memoization     | 493 ms                                                                 | 495 ms: 1.00x slower                                                     |
| xml_etree_parse            | 131 ms                                                                 | 132 ms: 1.01x slower                                                     |
| telco                      | 8.96 ms                                                                | 9.01 ms: 1.01x slower                                                    |
| python_startup             | 17.5 ms                                                                | 17.6 ms: 1.01x slower                                                    |
| tomli_loads                | 2.91 sec                                                               | 2.92 sec: 1.01x slower                                                   |
| pprint_safe_repr           | 1.07 sec                                                               | 1.08 sec: 1.01x slower                                                   |
| sphinx                     | 1.23 sec                                                               | 1.24 sec: 1.01x slower                                                   |
| async_tree_none            | 401 ms                                                                 | 403 ms: 1.01x slower                                                     |
| many_optionals             | 1.36 ms                                                                | 1.37 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 150 ms                                                                 | 151 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 94.9 ms                                                                | 95.6 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 866 ms                                                                 | 871 ms: 1.01x slower                                                     |
| bench_mp_pool              | 110 ms                                                                 | 110 ms: 1.01x slower                                                     |
| python_startup_no_site     | 10.2 ms                                                                | 10.3 ms: 1.01x slower                                                    |
| deepcopy_reduce            | 3.70 us                                                                | 3.73 us: 1.01x slower                                                    |
| go                         | 282 ms                                                                 | 284 ms: 1.01x slower                                                     |
| genshi_xml                 | 67.5 ms                                                                | 68.1 ms: 1.01x slower                                                    |
| pprint_pformat             | 2.21 sec                                                               | 2.23 sec: 1.01x slower                                                   |
| 2to3                       | 379 ms                                                                 | 382 ms: 1.01x slower                                                     |
| genshi_text                | 34.3 ms                                                                | 34.6 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 368 ms                                                                 | 372 ms: 1.01x slower                                                     |
| sympy_expand               | 983 ms                                                                 | 992 ms: 1.01x slower                                                     |
| dulwich_log                | 98.6 ms                                                                | 99.5 ms: 1.01x slower                                                    |
| float                      | 142 ms                                                                 | 143 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 627 ms                                                                 | 634 ms: 1.01x slower                                                     |
| xml_etree_process          | 82.6 ms                                                                | 83.6 ms: 1.01x slower                                                    |
| async_generators           | 468 ms                                                                 | 474 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 659 ms                                                                 | 668 ms: 1.01x slower                                                     |
| pickle_pure_python         | 552 us                                                                 | 560 us: 1.01x slower                                                     |
| pidigits                   | 181 ms                                                                 | 184 ms: 1.01x slower                                                     |
| thrift                     | 1.19 ms                                                                | 1.21 ms: 1.02x slower                                                    |
| generators                 | 38.8 ms                                                                | 39.5 ms: 1.02x slower                                                    |
| subparsers                 | 32.7 ms                                                                | 33.2 ms: 1.02x slower                                                    |
| coroutines                 | 27.9 ms                                                                | 28.5 ms: 1.02x slower                                                    |
| richards_super             | 100 ms                                                                 | 102 ms: 1.02x slower                                                     |
| sqlite_synth               | 2.28 us                                                                | 2.34 us: 1.02x slower                                                    |
| pathlib                    | 20.4 ms                                                                | 20.8 ms: 1.02x slower                                                    |
| mako                       | 19.7 ms                                                                | 20.2 ms: 1.02x slower                                                    |
| create_gc_cycles           | 1.82 ms                                                                | 1.86 ms: 1.03x slower                                                    |
| typing_runtime_protocols   | 212 us                                                                 | 218 us: 1.03x slower                                                     |
| logging_simple             | 11.1 us                                                                | 11.5 us: 1.03x slower                                                    |
| logging_format             | 12.4 us                                                                | 12.8 us: 1.03x slower                                                    |
| richards                   | 83.4 ms                                                                | 86.4 ms: 1.04x slower                                                    |
| nbody                      | 142 ms                                                                 | 147 ms: 1.04x slower                                                     |
| regex_effbot               | 2.85 ms                                                                | 2.97 ms: 1.04x slower                                                    |
| regex_v8                   | 25.2 ms                                                                | 26.3 ms: 1.04x slower                                                    |
| mdp                        | 2.93 sec                                                               | 3.07 sec: 1.05x slower                                                   |
| gc_traversal               | 3.16 ms                                                                | 3.53 ms: 1.11x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (23): chaos, k_core, asyncio_websockets, async_tree_memoization_tg, json_dumps, sympy_sum, bench_thread_pool, xml_etree_generate, sqlglot_transpile, scimark_monte_carlo, comprehensions, coverage, docutils, sqlglot_optimize, deltablue, json, deepcopy, sqlglot_parse, sympy_integrate, regex_compile, meteor_contest, pylint, connected_components

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x