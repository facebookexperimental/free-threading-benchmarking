# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 7e3de44
- commit date: 2024-12-11
- overall geometric mean: 1.008x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 367 ms: 1.00x faster                                                     |
| html5lib       | 97.9 ms                                                                | 97.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 388 ms                                                                 | 364 ms: 1.07x faster                                                     |
| async_tree_none_tg         | 358 ms                                                                 | 337 ms: 1.06x faster                                                     |
| async_tree_io              | 841 ms                                                                 | 795 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 822 ms                                                                 | 781 ms: 1.05x faster                                                     |
| async_tree_memoization     | 469 ms                                                                 | 448 ms: 1.05x faster                                                     |
| async_tree_memoization_tg  | 445 ms                                                                 | 425 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 612 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 594 ms: 1.04x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (3): asyncio_websockets, coroutines, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 137 ms                                                                 | 115 ms: 1.20x faster                                                     |
| nbody          | 128 ms                                                                 | 129 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                 | 181 ms: 1.01x slower                                                     |
| regex_v8       | 24.4 ms                                                                | 25.2 ms: 1.03x slower                                                    |
| regex_dna      | 182 ms                                                                 | 191 ms: 1.05x slower                                                     |
| regex_effbot   | 2.79 ms                                                                | 2.93 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 515 us                                                                 | 499 us: 1.03x faster                                                     |
| tomli_loads          | 2.67 sec                                                               | 2.62 sec: 1.02x faster                                                   |
| xml_etree_iterparse  | 91.3 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| xml_etree_parse      | 131 ms                                                                 | 131 ms: 1.01x faster                                                     |
| unpickle_pure_python | 333 us                                                                 | 331 us: 1.01x faster                                                     |
| xml_etree_generate   | 97.3 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| xml_etree_process    | 77.9 ms                                                                | 78.9 ms: 1.01x slower                                                    |
| json_dumps           | 14.2 ms                                                                | 14.4 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 51.2 ms                                                                | 50.2 ms: 1.02x faster                                                    |
| genshi_text     | 31.9 ms                                                                | 31.5 ms: 1.02x faster                                                    |
| mako            | 17.7 ms                                                                | 17.8 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 137 ms                                                                 | 115 ms: 1.20x faster                                                     |
| sqlglot_parse              | 2.58 ms                                                                | 2.35 ms: 1.10x faster                                                    |
| sqlglot_transpile          | 2.93 ms                                                                | 2.72 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult    | 6.04 ms                                                                | 5.66 ms: 1.07x faster                                                    |
| async_tree_none            | 388 ms                                                                 | 364 ms: 1.07x faster                                                     |
| mdp                        | 2.89 sec                                                               | 2.72 sec: 1.06x faster                                                   |
| async_tree_none_tg         | 358 ms                                                                 | 337 ms: 1.06x faster                                                     |
| async_tree_io              | 841 ms                                                                 | 795 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 822 ms                                                                 | 781 ms: 1.05x faster                                                     |
| async_tree_memoization     | 469 ms                                                                 | 448 ms: 1.05x faster                                                     |
| async_tree_memoization_tg  | 445 ms                                                                 | 425 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 612 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 594 ms: 1.04x faster                                                     |
| pickle_pure_python         | 515 us                                                                 | 499 us: 1.03x faster                                                     |
| dulwich_log                | 95.9 ms                                                                | 93.4 ms: 1.03x faster                                                    |
| logging_silent             | 185 ns                                                                 | 180 ns: 1.03x faster                                                     |
| sqlalchemy_imperative      | 29.8 ms                                                                | 29.1 ms: 1.02x faster                                                    |
| spectral_norm              | 123 ms                                                                 | 120 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.86 ms                                                                | 1.82 ms: 1.02x faster                                                    |
| django_template            | 51.2 ms                                                                | 50.2 ms: 1.02x faster                                                    |
| tomli_loads                | 2.67 sec                                                               | 2.62 sec: 1.02x faster                                                   |
| pathlib                    | 20.2 ms                                                                | 19.8 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 970 ms                                                                 | 955 ms: 1.02x faster                                                     |
| genshi_text                | 31.9 ms                                                                | 31.5 ms: 1.02x faster                                                    |
| meteor_contest             | 131 ms                                                                 | 129 ms: 1.01x faster                                                     |
| hexiom                     | 9.88 ms                                                                | 9.74 ms: 1.01x faster                                                    |
| scimark_sor                | 236 ms                                                                 | 232 ms: 1.01x faster                                                     |
| comprehensions             | 27.4 us                                                                | 27.1 us: 1.01x faster                                                    |
| xml_etree_iterparse        | 91.3 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| pprint_pformat             | 2.02 sec                                                               | 1.99 sec: 1.01x faster                                                   |
| crypto_pyaes               | 92.1 ms                                                                | 91.2 ms: 1.01x faster                                                    |
| gc_traversal               | 3.54 ms                                                                | 3.51 ms: 1.01x faster                                                    |
| generators                 | 38.0 ms                                                                | 37.7 ms: 1.01x faster                                                    |
| xml_etree_parse            | 131 ms                                                                 | 131 ms: 1.01x faster                                                     |
| html5lib                   | 97.9 ms                                                                | 97.3 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 333 us                                                                 | 331 us: 1.01x faster                                                     |
| scimark_fft                | 398 ms                                                                 | 396 ms: 1.00x faster                                                     |
| sympy_integrate            | 29.6 ms                                                                | 29.4 ms: 1.00x faster                                                    |
| sqlalchemy_declarative     | 203 ms                                                                 | 202 ms: 1.00x faster                                                     |
| sympy_sum                  | 350 ms                                                                 | 349 ms: 1.00x faster                                                     |
| sympy_expand               | 955 ms                                                                 | 952 ms: 1.00x faster                                                     |
| 2to3                       | 367 ms                                                                 | 367 ms: 1.00x faster                                                     |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| nbody                      | 128 ms                                                                 | 129 ms: 1.00x slower                                                     |
| many_optionals             | 1.29 ms                                                                | 1.29 ms: 1.00x slower                                                    |
| deepcopy_memo              | 39.6 us                                                                | 39.8 us: 1.01x slower                                                    |
| nqueens                    | 97.4 ms                                                                | 98.0 ms: 1.01x slower                                                    |
| json                       | 5.02 ms                                                                | 5.05 ms: 1.01x slower                                                    |
| regex_compile              | 180 ms                                                                 | 181 ms: 1.01x slower                                                     |
| xml_etree_generate         | 97.3 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| mako                       | 17.7 ms                                                                | 17.8 ms: 1.01x slower                                                    |
| scimark_lu                 | 184 ms                                                                 | 186 ms: 1.01x slower                                                     |
| go                         | 267 ms                                                                 | 269 ms: 1.01x slower                                                     |
| deltablue                  | 8.00 ms                                                                | 8.09 ms: 1.01x slower                                                    |
| chaos                      | 104 ms                                                                 | 105 ms: 1.01x slower                                                     |
| xml_etree_process          | 77.9 ms                                                                | 78.9 ms: 1.01x slower                                                    |
| json_dumps                 | 14.2 ms                                                                | 14.4 ms: 1.01x slower                                                    |
| scimark_monte_carlo        | 118 ms                                                                 | 120 ms: 1.02x slower                                                     |
| thrift                     | 1.16 ms                                                                | 1.19 ms: 1.02x slower                                                    |
| logging_simple             | 10.6 us                                                                | 10.8 us: 1.02x slower                                                    |
| richards_super             | 86.2 ms                                                                | 88.4 ms: 1.03x slower                                                    |
| raytrace                   | 547 ms                                                                 | 562 ms: 1.03x slower                                                     |
| richards                   | 76.7 ms                                                                | 79.0 ms: 1.03x slower                                                    |
| regex_v8                   | 24.4 ms                                                                | 25.2 ms: 1.03x slower                                                    |
| regex_dna                  | 182 ms                                                                 | 191 ms: 1.05x slower                                                     |
| regex_effbot               | 2.79 ms                                                                | 2.93 ms: 1.05x slower                                                    |
| coverage                   | 99.5 ms                                                                | 105 ms: 1.06x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (28): pylint, asyncio_websockets, docutils, sqlite_synth, genshi_xml, sympy_str, bench_thread_pool, sphinx, bpe_tokeniser, json_loads, subparsers, deepcopy_reduce, deepcopy, sqlglot_optimize, fannkuch, k_core, pyflate, coroutines, pidigits, bench_mp_pool, pycparser, async_generators, sqlglot_normalize, connected_components, shortest_path, typing_runtime_protocols, telco, logging_format

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x