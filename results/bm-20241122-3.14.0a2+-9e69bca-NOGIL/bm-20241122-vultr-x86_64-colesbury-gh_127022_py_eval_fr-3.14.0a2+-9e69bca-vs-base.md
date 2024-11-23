# Results vs. base

- fork: colesbury
- ref: gh_127022_py_eval_fr
- machine: linux-x86_64
- commit hash: 9e69bca
- commit date: 2024-11-22
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 374 ms                                                                 | 380 ms: 1.02x slower                                                      |
| html5lib       | 101 ms                                                                 | 103 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 409 ms                                                                 | 401 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed_tg | 639 ms                                                                 | 628 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed    | 663 ms                                                                 | 653 ms: 1.02x faster                                                      |
| async_tree_none_tg         | 375 ms                                                                 | 369 ms: 1.01x faster                                                      |
| async_tree_memoization     | 496 ms                                                                 | 491 ms: 1.01x faster                                                      |
| async_tree_io_tg           | 871 ms                                                                 | 865 ms: 1.01x faster                                                      |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                      |
| coroutines                 | 27.4 ms                                                                | 28.0 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (3): async_tree_io, async_generators, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 142 ms                                                                 | 144 ms: 1.01x slower                                                      |
| pidigits       | 181 ms                                                                 | 185 ms: 1.02x slower                                                      |
| nbody          | 156 ms                                                                 | 160 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 24.9 ms                                                                | 24.5 ms: 1.02x faster                                                     |
| regex_effbot   | 2.74 ms                                                                | 2.71 ms: 1.01x faster                                                     |
| regex_dna      | 184 ms                                                                 | 182 ms: 1.01x faster                                                      |
| regex_compile  | 193 ms                                                                 | 195 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_process    | 81.6 ms                                                                | 82.2 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.5 ms: 1.01x slower                                                     |
| json_dumps           | 14.4 ms                                                                | 14.5 ms: 1.01x slower                                                     |
| tomli_loads          | 2.88 sec                                                               | 2.95 sec: 1.02x slower                                                    |
| pickle_pure_python   | 542 us                                                                 | 562 us: 1.04x slower                                                      |
| unpickle_pure_python | 360 us                                                                 | 378 us: 1.05x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (3): json_loads, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.6 ms: 1.01x slower                                                     |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                     |
| django_template | 55.2 ms                                                                | 55.7 ms: 1.01x slower                                                     |
| mako            | 19.4 ms                                                                | 19.7 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2+-4759ba6 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 5.71 ms                                                                | 5.56 ms: 1.03x faster                                                     |
| scimark_lu                 | 201 ms                                                                 | 196 ms: 1.02x faster                                                      |
| async_tree_none            | 409 ms                                                                 | 401 ms: 1.02x faster                                                      |
| regex_v8                   | 24.9 ms                                                                | 24.5 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed_tg | 639 ms                                                                 | 628 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed    | 663 ms                                                                 | 653 ms: 1.02x faster                                                      |
| async_tree_none_tg         | 375 ms                                                                 | 369 ms: 1.01x faster                                                      |
| regex_effbot               | 2.74 ms                                                                | 2.71 ms: 1.01x faster                                                     |
| telco                      | 9.00 ms                                                                | 8.89 ms: 1.01x faster                                                     |
| regex_dna                  | 184 ms                                                                 | 182 ms: 1.01x faster                                                      |
| bench_thread_pool          | 3.41 ms                                                                | 3.38 ms: 1.01x faster                                                     |
| async_tree_memoization     | 496 ms                                                                 | 491 ms: 1.01x faster                                                      |
| pathlib                    | 20.8 ms                                                                | 20.6 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 871 ms                                                                 | 865 ms: 1.01x faster                                                      |
| genshi_xml                 | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                     |
| asyncio_websockets         | 522 ms                                                                 | 519 ms: 1.01x faster                                                      |
| logging_silent             | 193 ns                                                                 | 194 ns: 1.00x slower                                                      |
| dulwich_log                | 98.4 ms                                                                | 98.8 ms: 1.00x slower                                                     |
| chaos                      | 114 ms                                                                 | 115 ms: 1.00x slower                                                      |
| subparsers                 | 33.0 ms                                                                | 33.2 ms: 1.01x slower                                                     |
| connected_components       | 508 ms                                                                 | 511 ms: 1.01x slower                                                      |
| json                       | 5.02 ms                                                                | 5.05 ms: 1.01x slower                                                     |
| python_startup             | 17.5 ms                                                                | 17.6 ms: 1.01x slower                                                     |
| mdp                        | 2.92 sec                                                               | 2.94 sec: 1.01x slower                                                    |
| xml_etree_process          | 81.6 ms                                                                | 82.2 ms: 1.01x slower                                                     |
| k_core                     | 2.49 sec                                                               | 2.50 sec: 1.01x slower                                                    |
| deepcopy                   | 355 us                                                                 | 358 us: 1.01x slower                                                      |
| sympy_integrate            | 31.2 ms                                                                | 31.4 ms: 1.01x slower                                                     |
| sqlglot_normalize          | 149 ms                                                                 | 150 ms: 1.01x slower                                                      |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.01x slower                                                     |
| sqlite_synth               | 2.30 us                                                                | 2.32 us: 1.01x slower                                                     |
| thrift                     | 1.20 ms                                                                | 1.21 ms: 1.01x slower                                                     |
| many_optionals             | 1.36 ms                                                                | 1.38 ms: 1.01x slower                                                     |
| regex_compile              | 193 ms                                                                 | 195 ms: 1.01x slower                                                      |
| coverage                   | 102 ms                                                                 | 103 ms: 1.01x slower                                                      |
| shortest_path              | 559 ms                                                                 | 564 ms: 1.01x slower                                                      |
| bench_mp_pool              | 110 ms                                                                 | 111 ms: 1.01x slower                                                      |
| django_template            | 55.2 ms                                                                | 55.7 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 210 us                                                                 | 212 us: 1.01x slower                                                      |
| logging_simple             | 11.0 us                                                                | 11.1 us: 1.01x slower                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.5 ms: 1.01x slower                                                     |
| sqlglot_optimize           | 74.8 ms                                                                | 75.6 ms: 1.01x slower                                                     |
| json_dumps                 | 14.4 ms                                                                | 14.5 ms: 1.01x slower                                                     |
| comprehensions             | 28.6 us                                                                | 29.0 us: 1.01x slower                                                     |
| float                      | 142 ms                                                                 | 144 ms: 1.01x slower                                                      |
| bpe_tokeniser              | 5.54 sec                                                               | 5.62 sec: 1.01x slower                                                    |
| sqlglot_transpile          | 3.03 ms                                                                | 3.08 ms: 1.02x slower                                                     |
| sqlglot_parse              | 2.63 ms                                                                | 2.67 ms: 1.02x slower                                                     |
| 2to3                       | 374 ms                                                                 | 380 ms: 1.02x slower                                                      |
| hexiom                     | 11.3 ms                                                                | 11.5 ms: 1.02x slower                                                     |
| mako                       | 19.4 ms                                                                | 19.7 ms: 1.02x slower                                                     |
| pidigits                   | 181 ms                                                                 | 185 ms: 1.02x slower                                                      |
| html5lib                   | 101 ms                                                                 | 103 ms: 1.02x slower                                                      |
| pprint_pformat             | 2.18 sec                                                               | 2.23 sec: 1.02x slower                                                    |
| crypto_pyaes               | 101 ms                                                                 | 103 ms: 1.02x slower                                                      |
| create_gc_cycles           | 1.82 ms                                                                | 1.86 ms: 1.02x slower                                                     |
| coroutines                 | 27.4 ms                                                                | 28.0 ms: 1.02x slower                                                     |
| tomli_loads                | 2.88 sec                                                               | 2.95 sec: 1.02x slower                                                    |
| scimark_monte_carlo        | 119 ms                                                                 | 122 ms: 1.02x slower                                                      |
| nqueens                    | 108 ms                                                                 | 110 ms: 1.03x slower                                                      |
| nbody                      | 156 ms                                                                 | 160 ms: 1.03x slower                                                      |
| raytrace                   | 591 ms                                                                 | 608 ms: 1.03x slower                                                      |
| spectral_norm              | 129 ms                                                                 | 132 ms: 1.03x slower                                                      |
| pyflate                    | 729 ms                                                                 | 750 ms: 1.03x slower                                                      |
| pprint_safe_repr           | 1.05 sec                                                               | 1.08 sec: 1.03x slower                                                    |
| scimark_fft                | 393 ms                                                                 | 406 ms: 1.03x slower                                                      |
| generators                 | 39.3 ms                                                                | 40.6 ms: 1.04x slower                                                     |
| richards_super             | 96.5 ms                                                                | 99.9 ms: 1.04x slower                                                     |
| pickle_pure_python         | 542 us                                                                 | 562 us: 1.04x slower                                                      |
| deltablue                  | 8.49 ms                                                                | 8.80 ms: 1.04x slower                                                     |
| go                         | 275 ms                                                                 | 287 ms: 1.04x slower                                                      |
| deepcopy_memo              | 43.7 us                                                                | 45.7 us: 1.04x slower                                                     |
| unpickle_pure_python       | 360 us                                                                 | 378 us: 1.05x slower                                                      |
| richards                   | 80.2 ms                                                                | 84.5 ms: 1.05x slower                                                     |
| gc_traversal               | 3.19 ms                                                                | 3.52 ms: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (19): meteor_contest, deepcopy_reduce, async_tree_io, sympy_expand, json_loads, sympy_str, genshi_text, pycparser, logging_format, fannkuch, xml_etree_parse, xml_etree_generate, async_generators, sympy_sum, async_tree_memoization_tg, sphinx, docutils, scimark_sor, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x