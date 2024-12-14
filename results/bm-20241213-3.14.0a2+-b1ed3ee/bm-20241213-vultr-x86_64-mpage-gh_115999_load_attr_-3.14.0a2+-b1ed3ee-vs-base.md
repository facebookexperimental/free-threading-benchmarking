# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 254 ms: 1.00x faster                                                  |
| docutils       | 2.55 sec                                                               | 2.54 sec: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 310 ms                                                                 | 303 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 614 ms                                                                 | 603 ms: 1.02x faster                                                  |
| async_tree_io              | 631 ms                                                                 | 619 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 496 ms: 1.02x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 275 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 253 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 479 ms: 1.02x faster                                                  |
| async_tree_memoization     | 335 ms                                                                 | 330 ms: 1.02x faster                                                  |
| async_generators           | 359 ms                                                                 | 354 ms: 1.01x faster                                                  |
| coroutines                 | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 90.0 ms                                                                | 88.8 ms: 1.01x faster                                                 |
| pidigits       | 185 ms                                                                 | 186 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| regex_v8       | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 321 us                                                                 | 315 us: 1.02x faster                                                  |
| json_loads           | 26.2 us                                                                | 25.9 us: 1.01x faster                                                 |
| unpickle_pure_python | 211 us                                                                 | 209 us: 1.01x faster                                                  |
| xml_etree_generate   | 82.9 ms                                                                | 83.2 ms: 1.00x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): xml_etree_process, xml_etree_iterparse, tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.51 ms                                                                | 7.48 ms: 1.00x faster                                                 |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                | 35.6 ms: 1.01x faster                                                 |
| mako            | 11.6 ms                                                                | 11.5 ms: 1.00x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_sor                | 127 ms                                                                 | 119 ms: 1.07x faster                                                  |
| mdp                        | 2.46 sec                                                               | 2.31 sec: 1.06x faster                                                |
| spectral_norm              | 101 ms                                                                 | 94.9 ms: 1.06x faster                                                 |
| logging_silent             | 106 ns                                                                 | 101 ns: 1.06x faster                                                  |
| thrift                     | 758 us                                                                 | 723 us: 1.05x faster                                                  |
| richards                   | 45.1 ms                                                                | 43.5 ms: 1.04x faster                                                 |
| regex_effbot               | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| deepcopy_memo              | 29.8 us                                                                | 29.0 us: 1.03x faster                                                 |
| richards_super             | 50.9 ms                                                                | 49.5 ms: 1.03x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| scimark_fft                | 318 ms                                                                 | 311 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 303 ms: 1.02x faster                                                  |
| fannkuch                   | 378 ms                                                                 | 370 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.43 sec: 1.02x faster                                                |
| regex_dna                  | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 614 ms                                                                 | 603 ms: 1.02x faster                                                  |
| async_tree_io              | 631 ms                                                                 | 619 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 496 ms: 1.02x faster                                                  |
| nqueens                    | 80.6 ms                                                                | 79.1 ms: 1.02x faster                                                 |
| go                         | 117 ms                                                                 | 115 ms: 1.02x faster                                                  |
| pickle_pure_python         | 321 us                                                                 | 315 us: 1.02x faster                                                  |
| chaos                      | 58.6 ms                                                                | 57.6 ms: 1.02x faster                                                 |
| async_tree_none            | 280 ms                                                                 | 275 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 253 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 479 ms: 1.02x faster                                                  |
| async_tree_memoization     | 335 ms                                                                 | 330 ms: 1.02x faster                                                  |
| async_generators           | 359 ms                                                                 | 354 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 2.58 us                                                                | 2.54 us: 1.01x faster                                                 |
| deepcopy                   | 253 us                                                                 | 249 us: 1.01x faster                                                  |
| nbody                      | 90.0 ms                                                                | 88.8 ms: 1.01x faster                                                 |
| django_template            | 36.1 ms                                                                | 35.6 ms: 1.01x faster                                                 |
| sympy_str                  | 273 ms                                                                 | 270 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 712 ms                                                                 | 704 ms: 1.01x faster                                                  |
| hexiom                     | 5.86 ms                                                                | 5.79 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 104 ms                                                                 | 103 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.0 ms                                                                | 66.4 ms: 1.01x faster                                                 |
| json_loads                 | 26.2 us                                                                | 25.9 us: 1.01x faster                                                 |
| sqlite_synth               | 2.19 us                                                                | 2.17 us: 1.01x faster                                                 |
| scimark_lu                 | 110 ms                                                                 | 109 ms: 1.01x faster                                                  |
| dulwich_log                | 75.7 ms                                                                | 75.2 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 211 us                                                                 | 209 us: 1.01x faster                                                  |
| sympy_sum                  | 153 ms                                                                 | 152 ms: 1.01x faster                                                  |
| sympy_expand               | 459 ms                                                                 | 456 ms: 1.01x faster                                                  |
| comprehensions             | 17.2 us                                                                | 17.1 us: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.12 sec: 1.01x faster                                                |
| shortest_path              | 438 ms                                                                 | 436 ms: 1.00x faster                                                  |
| docutils                   | 2.55 sec                                                               | 2.54 sec: 1.00x faster                                                |
| mako                       | 11.6 ms                                                                | 11.5 ms: 1.00x faster                                                 |
| many_optionals             | 1.03 ms                                                                | 1.02 ms: 1.00x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                                | 1.56 ms: 1.00x faster                                                 |
| python_startup_no_site     | 7.51 ms                                                                | 7.48 ms: 1.00x faster                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 52.0 ms: 1.00x faster                                                 |
| sympy_integrate            | 19.9 ms                                                                | 19.8 ms: 1.00x faster                                                 |
| 2to3                       | 255 ms                                                                 | 254 ms: 1.00x faster                                                  |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| pidigits                   | 185 ms                                                                 | 186 ms: 1.00x slower                                                  |
| xml_etree_generate         | 82.9 ms                                                                | 83.2 ms: 1.00x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 156 us: 1.01x slower                                                  |
| pyflate                    | 423 ms                                                                 | 426 ms: 1.01x slower                                                  |
| telco                      | 7.10 ms                                                                | 7.17 ms: 1.01x slower                                                 |
| coroutines                 | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                 |
| generators                 | 27.1 ms                                                                | 27.3 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.21 sec                                                               | 4.26 sec: 1.01x slower                                                |
| json_dumps                 | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 19.3 ms: 1.01x slower                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 128 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.22 ms                                                                | 4.30 ms: 1.02x slower                                                 |
| logging_format             | 6.83 us                                                                | 7.00 us: 1.02x slower                                                 |
| logging_simple             | 6.02 us                                                                | 6.23 us: 1.04x slower                                                 |
| gc_traversal               | 4.02 ms                                                                | 4.41 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (25): k_core, float, raytrace, sphinx, genshi_text, bench_mp_pool, connected_components, create_gc_cycles, xml_etree_process, coverage, json, subparsers, pathlib, regex_compile, deltablue, pylint, bench_thread_pool, sqlglot_parse, asyncio_websockets, genshi_xml, xml_etree_iterparse, tomli_loads, scimark_monte_carlo, meteor_contest, xml_etree_parse

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x