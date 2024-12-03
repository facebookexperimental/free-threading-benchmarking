# Results vs. base

- fork: nascheme
- ref: gh_127271_cell_get_s
- machine: linux-x86_64
- commit hash: b09c4cf
- commit date: 2024-11-27
- overall geometric mean: 1.004x slower
- HPT reliability: 82.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 22.6 ms                                                                | 21.8 ms: 1.03x faster                                                    |
| async_generators           | 371 ms                                                                 | 373 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 664 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed    | 574 ms                                                                 | 669 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (7): async_tree_io, async_tree_none, asyncio_websockets, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.1 ms                                                                | 81.4 ms: 1.02x slower                                                    |
| nbody          | 93.9 ms                                                                | 95.9 ms: 1.02x slower                                                    |
| pidigits       | 185 ms                                                                 | 226 ms: 1.22x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.90 ms                                                                | 2.73 ms: 1.06x faster                                                    |
| regex_v8       | 24.1 ms                                                                | 23.3 ms: 1.04x faster                                                    |
| regex_dna      | 180 ms                                                                 | 179 ms: 1.00x faster                                                     |
| regex_compile  | 130 ms                                                                 | 135 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads         | 25.1 us                                                                | 24.9 us: 1.01x faster                                                    |
| json_dumps         | 11.5 ms                                                                | 11.5 ms: 1.00x slower                                                    |
| xml_etree_generate | 85.9 ms                                                                | 86.4 ms: 1.01x slower                                                    |
| xml_etree_process  | 60.6 ms                                                                | 61.0 ms: 1.01x slower                                                    |
| tomli_loads        | 2.11 sec                                                               | 2.13 sec: 1.01x slower                                                   |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (4): unpickle_pure_python, xml_etree_iterparse, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.3 ms                                                                | 49.7 ms: 1.01x faster                                                    |
| mako            | 11.6 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| django_template | 35.1 ms                                                                | 36.1 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2+-6da9d25 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.15 ms                                                                | 3.74 ms: 1.11x faster                                                    |
| regex_effbot               | 2.90 ms                                                                | 2.73 ms: 1.06x faster                                                    |
| mdp                        | 2.48 sec                                                               | 2.35 sec: 1.06x faster                                                   |
| regex_v8                   | 24.1 ms                                                                | 23.3 ms: 1.04x faster                                                    |
| coroutines                 | 22.6 ms                                                                | 21.8 ms: 1.03x faster                                                    |
| deepcopy_reduce            | 2.66 us                                                                | 2.59 us: 1.03x faster                                                    |
| logging_simple             | 6.32 us                                                                | 6.16 us: 1.03x faster                                                    |
| json                       | 4.60 ms                                                                | 4.50 ms: 1.02x faster                                                    |
| meteor_contest             | 102 ms                                                                 | 99.4 ms: 1.02x faster                                                    |
| pycparser                  | 1.14 sec                                                               | 1.12 sec: 1.01x faster                                                   |
| genshi_xml                 | 50.3 ms                                                                | 49.7 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 723 ms                                                                 | 716 ms: 1.01x faster                                                     |
| json_loads                 | 25.1 us                                                                | 24.9 us: 1.01x faster                                                    |
| spectral_norm              | 111 ms                                                                 | 110 ms: 1.01x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                   |
| richards                   | 46.7 ms                                                                | 46.4 ms: 1.01x faster                                                    |
| telco                      | 7.34 ms                                                                | 7.28 ms: 1.01x faster                                                    |
| chaos                      | 59.3 ms                                                                | 58.8 ms: 1.01x faster                                                    |
| create_gc_cycles           | 1.96 ms                                                                | 1.94 ms: 1.01x faster                                                    |
| deepcopy                   | 262 us                                                                 | 260 us: 1.01x faster                                                     |
| pathlib                    | 18.4 ms                                                                | 18.3 ms: 1.01x faster                                                    |
| shortest_path              | 446 ms                                                                 | 444 ms: 1.01x faster                                                     |
| go                         | 121 ms                                                                 | 120 ms: 1.00x faster                                                     |
| regex_dna                  | 180 ms                                                                 | 179 ms: 1.00x faster                                                     |
| logging_silent             | 107 ns                                                                 | 107 ns: 1.00x faster                                                     |
| crypto_pyaes               | 68.0 ms                                                                | 67.8 ms: 1.00x faster                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                    |
| pylint                     | 269 ms                                                                 | 269 ms: 1.00x slower                                                     |
| sqlalchemy_declarative     | 126 ms                                                                 | 126 ms: 1.00x slower                                                     |
| sqlglot_transpile          | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                    |
| sqlglot_normalize          | 107 ms                                                                 | 107 ms: 1.00x slower                                                     |
| sympy_sum                  | 153 ms                                                                 | 153 ms: 1.00x slower                                                     |
| raytrace                   | 264 ms                                                                 | 265 ms: 1.00x slower                                                     |
| pyflate                    | 449 ms                                                                 | 451 ms: 1.00x slower                                                     |
| json_dumps                 | 11.5 ms                                                                | 11.5 ms: 1.00x slower                                                    |
| sqlglot_parse              | 1.29 ms                                                                | 1.30 ms: 1.01x slower                                                    |
| scimark_fft                | 338 ms                                                                 | 340 ms: 1.01x slower                                                     |
| xml_etree_generate         | 85.9 ms                                                                | 86.4 ms: 1.01x slower                                                    |
| bpe_tokeniser              | 4.43 sec                                                               | 4.46 sec: 1.01x slower                                                   |
| xml_etree_process          | 60.6 ms                                                                | 61.0 ms: 1.01x slower                                                    |
| async_generators           | 371 ms                                                                 | 373 ms: 1.01x slower                                                     |
| sqlglot_optimize           | 53.5 ms                                                                | 53.9 ms: 1.01x slower                                                    |
| scimark_monte_carlo        | 65.5 ms                                                                | 66.0 ms: 1.01x slower                                                    |
| richards_super             | 53.0 ms                                                                | 53.5 ms: 1.01x slower                                                    |
| tomli_loads                | 2.11 sec                                                               | 2.13 sec: 1.01x slower                                                   |
| deepcopy_memo              | 30.0 us                                                                | 30.3 us: 1.01x slower                                                    |
| comprehensions             | 17.3 us                                                                | 17.5 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 4.43 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 157 us                                                                 | 159 us: 1.01x slower                                                     |
| sqlite_synth               | 2.20 us                                                                | 2.23 us: 1.01x slower                                                    |
| float                      | 80.1 ms                                                                | 81.4 ms: 1.02x slower                                                    |
| nbody                      | 93.9 ms                                                                | 95.9 ms: 1.02x slower                                                    |
| mako                       | 11.6 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| fannkuch                   | 377 ms                                                                 | 386 ms: 1.02x slower                                                     |
| django_template            | 35.1 ms                                                                | 36.1 ms: 1.03x slower                                                    |
| regex_compile              | 130 ms                                                                 | 135 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 664 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed    | 574 ms                                                                 | 669 ms: 1.17x slower                                                     |
| pidigits                   | 185 ms                                                                 | 226 ms: 1.22x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (36): async_tree_io, thrift, scimark_lu, sphinx, subparsers, bench_mp_pool, sympy_expand, logging_format, unpickle_pure_python, k_core, scimark_sor, hexiom, generators, 2to3, bench_thread_pool, python_startup, async_tree_none, sqlalchemy_imperative, coverage, nqueens, genshi_text, many_optionals, sympy_integrate, deltablue, asyncio_websockets, xml_etree_iterparse, pickle_pure_python, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, dulwich_log, sympy_str, xml_etree_parse, connected_components, pprint_pformat, async_tree_io_tg

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 82.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x