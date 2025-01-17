# Results vs. base

- fork: mpage
- ref: aa_test_0
- machine: linux-x86_64
- commit hash: 54bb905
- commit date: 2025-01-16
- overall geometric mean: 1.007x slower
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| coroutines                 | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                      |
| async_tree_memoization_tg  | 302 ms                                                                 | 306 ms: 1.01x slower                                       |
| async_tree_io_tg           | 605 ms                                                                 | 614 ms: 1.02x slower                                       |
| async_tree_none_tg         | 252 ms                                                                 | 256 ms: 1.02x slower                                       |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 565 ms: 1.20x slower                                       |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 587 ms: 1.20x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                               |

Benchmark hidden because not significant (5): asyncio_websockets, async_generators, async_tree_memoization, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 71.3 ms                                                                | 73.0 ms: 1.02x slower                                      |
| nbody          | 85.8 ms                                                                | 88.3 ms: 1.03x slower                                      |
| pidigits       | 206 ms                                                                 | 227 ms: 1.10x slower                                       |
| Geometric mean | (ref)                                                                  | 1.05x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.77 ms: 1.02x faster                                      |
| regex_compile  | 128 ms                                                                 | 127 ms: 1.00x faster                                       |
| regex_dna      | 171 ms                                                                 | 173 ms: 1.01x slower                                       |
| regex_v8       | 23.8 ms                                                                | 24.8 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| unpickle_pure_python | 216 us                                                                 | 213 us: 1.01x faster                                       |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                       |
| json_loads           | 27.8 us                                                                | 27.6 us: 1.01x faster                                      |
| json_dumps           | 11.4 ms                                                                | 11.4 ms: 1.00x faster                                      |
| xml_etree_iterparse  | 90.9 ms                                                                | 91.4 ms: 1.01x slower                                      |
| pickle_pure_python   | 308 us                                                                 | 320 us: 1.04x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.45 ms                                                                | 7.43 ms: 1.00x faster                                      |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                      |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 21.6 ms                                                                | 21.3 ms: 1.01x faster                                      |
| django_template | 35.7 ms                                                                | 36.1 ms: 1.01x slower                                      |
| mako            | 11.7 ms                                                                | 11.9 ms: 1.01x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mdp                        | 2.46 sec                                                               | 2.37 sec: 1.04x faster                                     |
| scimark_fft                | 328 ms                                                                 | 317 ms: 1.04x faster                                       |
| coroutines                 | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                      |
| gc_traversal               | 4.32 ms                                                                | 4.21 ms: 1.03x faster                                      |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 4.48 ms: 1.03x faster                                      |
| regex_effbot               | 2.84 ms                                                                | 2.77 ms: 1.02x faster                                      |
| telco                      | 7.33 ms                                                                | 7.18 ms: 1.02x faster                                      |
| pathlib                    | 18.3 ms                                                                | 18.0 ms: 1.02x faster                                      |
| scimark_lu                 | 115 ms                                                                 | 113 ms: 1.01x faster                                       |
| unpickle_pure_python       | 216 us                                                                 | 213 us: 1.01x faster                                       |
| genshi_text                | 21.6 ms                                                                | 21.3 ms: 1.01x faster                                      |
| sqlalchemy_imperative      | 19.5 ms                                                                | 19.3 ms: 1.01x faster                                      |
| pyflate                    | 409 ms                                                                 | 405 ms: 1.01x faster                                       |
| sqlite_synth               | 2.22 us                                                                | 2.20 us: 1.01x faster                                      |
| scimark_monte_carlo        | 64.4 ms                                                                | 63.8 ms: 1.01x faster                                      |
| create_gc_cycles           | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                      |
| fannkuch                   | 375 ms                                                                 | 372 ms: 1.01x faster                                       |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                       |
| json_loads                 | 27.8 us                                                                | 27.6 us: 1.01x faster                                      |
| regex_compile              | 128 ms                                                                 | 127 ms: 1.00x faster                                       |
| crypto_pyaes               | 66.6 ms                                                                | 66.2 ms: 1.00x faster                                      |
| json_dumps                 | 11.4 ms                                                                | 11.4 ms: 1.00x faster                                      |
| python_startup_no_site     | 7.45 ms                                                                | 7.43 ms: 1.00x faster                                      |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                      |
| go                         | 115 ms                                                                 | 115 ms: 1.00x slower                                       |
| scimark_sor                | 115 ms                                                                 | 115 ms: 1.00x slower                                       |
| xml_etree_iterparse        | 90.9 ms                                                                | 91.4 ms: 1.01x slower                                      |
| pprint_pformat             | 1.44 sec                                                               | 1.44 sec: 1.01x slower                                     |
| logging_simple             | 6.16 us                                                                | 6.20 us: 1.01x slower                                      |
| comprehensions             | 16.7 us                                                                | 16.9 us: 1.01x slower                                      |
| dulwich_log                | 76.1 ms                                                                | 76.6 ms: 1.01x slower                                      |
| shortest_path              | 430 ms                                                                 | 433 ms: 1.01x slower                                       |
| subparsers                 | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                      |
| sqlglot_transpile          | 1.55 ms                                                                | 1.56 ms: 1.01x slower                                      |
| connected_components       | 390 ms                                                                 | 393 ms: 1.01x slower                                       |
| sqlglot_optimize           | 52.4 ms                                                                | 52.8 ms: 1.01x slower                                      |
| django_template            | 35.7 ms                                                                | 36.1 ms: 1.01x slower                                      |
| hexiom                     | 5.73 ms                                                                | 5.79 ms: 1.01x slower                                      |
| sqlglot_parse              | 1.25 ms                                                                | 1.27 ms: 1.01x slower                                      |
| nqueens                    | 78.1 ms                                                                | 79.1 ms: 1.01x slower                                      |
| async_tree_memoization_tg  | 302 ms                                                                 | 306 ms: 1.01x slower                                       |
| logging_format             | 6.87 us                                                                | 6.97 us: 1.01x slower                                      |
| regex_dna                  | 171 ms                                                                 | 173 ms: 1.01x slower                                       |
| typing_runtime_protocols   | 156 us                                                                 | 158 us: 1.01x slower                                       |
| mako                       | 11.7 ms                                                                | 11.9 ms: 1.01x slower                                      |
| async_tree_io_tg           | 605 ms                                                                 | 614 ms: 1.02x slower                                       |
| raytrace                   | 261 ms                                                                 | 266 ms: 1.02x slower                                       |
| async_tree_none_tg         | 252 ms                                                                 | 256 ms: 1.02x slower                                       |
| meteor_contest             | 97.7 ms                                                                | 99.9 ms: 1.02x slower                                      |
| float                      | 71.3 ms                                                                | 73.0 ms: 1.02x slower                                      |
| deepcopy_memo              | 29.9 us                                                                | 30.6 us: 1.02x slower                                      |
| nbody                      | 85.8 ms                                                                | 88.3 ms: 1.03x slower                                      |
| pickle_pure_python         | 308 us                                                                 | 320 us: 1.04x slower                                       |
| regex_v8                   | 23.8 ms                                                                | 24.8 ms: 1.04x slower                                      |
| spectral_norm              | 88.3 ms                                                                | 92.3 ms: 1.04x slower                                      |
| generators                 | 28.0 ms                                                                | 29.5 ms: 1.06x slower                                      |
| pidigits                   | 206 ms                                                                 | 227 ms: 1.10x slower                                       |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 565 ms: 1.20x slower                                       |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 587 ms: 1.20x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (36): json, deltablue, docutils, pycparser, pylint, deepcopy, many_optionals, richards_super, xml_etree_generate, sqlalchemy_declarative, chaos, sqlglot_normalize, asyncio_websockets, bench_mp_pool, logging_silent, 2to3, bench_thread_pool, xml_etree_process, richards, bpe_tokeniser, k_core, tomli_loads, sympy_sum, sympy_integrate, thrift, deepcopy_reduce, sympy_str, coverage, pprint_safe_repr, genshi_xml, sympy_expand, sphinx, async_generators, async_tree_memoization, async_tree_io, async_tree_none

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 99.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x