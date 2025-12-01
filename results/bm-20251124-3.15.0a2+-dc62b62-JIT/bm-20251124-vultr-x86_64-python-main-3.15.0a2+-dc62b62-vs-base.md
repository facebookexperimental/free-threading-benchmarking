# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.002x faster
- HPT reliability: 76.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg          | 603 ms                                                                 | 595 ms: 1.01x faster                                   |
| async_generators          | 364 ms                                                                 | 360 ms: 1.01x faster                                   |
| async_tree_cpu_io_mixed   | 496 ms                                                                 | 490 ms: 1.01x faster                                   |
| async_tree_memoization_tg | 313 ms                                                                 | 310 ms: 1.01x faster                                   |
| coroutines                | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                  |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 90.3 ms                                                                | 88.0 ms: 1.03x faster                                  |
| pidigits       | 196 ms                                                                 | 195 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.67 ms: 1.04x faster                                  |
| regex_dna      | 180 ms                                                                 | 176 ms: 1.03x faster                                   |
| regex_v8       | 23.0 ms                                                                | 22.5 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps         | 9.24 ms                                                                | 9.06 ms: 1.02x faster                                  |
| xml_etree_parse    | 129 ms                                                                 | 128 ms: 1.01x faster                                   |
| xml_etree_generate | 76.9 ms                                                                | 77.4 ms: 1.01x slower                                  |
| xml_etree_process  | 53.3 ms                                                                | 53.6 ms: 1.01x slower                                  |
| json_loads         | 28.6 us                                                                | 28.8 us: 1.01x slower                                  |
| Geometric mean     | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (4): tomli_loads, pickle_pure_python, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 12.4 ms: 1.00x faster                                  |
| python_startup_no_site | 7.24 ms                                                                | 7.23 ms: 1.00x faster                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.4 ms: 1.03x faster                                  |
| genshi_xml      | 55.2 ms                                                                | 56.1 ms: 1.02x slower                                  |
| django_template | 34.4 ms                                                                | 35.1 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot              | 2.78 ms                                                                | 2.67 ms: 1.04x faster                                  |
| mako                      | 10.8 ms                                                                | 10.4 ms: 1.03x faster                                  |
| scimark_monte_carlo       | 57.3 ms                                                                | 55.8 ms: 1.03x faster                                  |
| regex_dna                 | 180 ms                                                                 | 176 ms: 1.03x faster                                   |
| nbody                     | 90.3 ms                                                                | 88.0 ms: 1.03x faster                                  |
| logging_simple            | 5.92 us                                                                | 5.77 us: 1.03x faster                                  |
| deepcopy_reduce           | 2.60 us                                                                | 2.54 us: 1.02x faster                                  |
| regex_v8                  | 23.0 ms                                                                | 22.5 ms: 1.02x faster                                  |
| json_dumps                | 9.24 ms                                                                | 9.06 ms: 1.02x faster                                  |
| logging_format            | 6.61 us                                                                | 6.48 us: 1.02x faster                                  |
| comprehensions            | 16.0 us                                                                | 15.7 us: 1.02x faster                                  |
| deepcopy                  | 251 us                                                                 | 247 us: 1.02x faster                                   |
| thrift                    | 751 us                                                                 | 739 us: 1.02x faster                                   |
| dulwich_log               | 74.9 ms                                                                | 73.9 ms: 1.01x faster                                  |
| async_tree_io_tg          | 603 ms                                                                 | 595 ms: 1.01x faster                                   |
| async_generators          | 364 ms                                                                 | 360 ms: 1.01x faster                                   |
| meteor_contest            | 98.1 ms                                                                | 97.0 ms: 1.01x faster                                  |
| async_tree_cpu_io_mixed   | 496 ms                                                                 | 490 ms: 1.01x faster                                   |
| bench_mp_pool             | 13.2 ms                                                                | 13.0 ms: 1.01x faster                                  |
| async_tree_memoization_tg | 313 ms                                                                 | 310 ms: 1.01x faster                                   |
| telco                     | 161 ms                                                                 | 160 ms: 1.01x faster                                   |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                   |
| create_gc_cycles          | 1.91 ms                                                                | 1.90 ms: 1.01x faster                                  |
| bpe_tokeniser             | 3.99 sec                                                               | 3.96 sec: 1.01x faster                                 |
| scimark_fft               | 258 ms                                                                 | 257 ms: 1.00x faster                                   |
| python_startup            | 12.4 ms                                                                | 12.4 ms: 1.00x faster                                  |
| pidigits                  | 196 ms                                                                 | 195 ms: 1.00x faster                                   |
| python_startup_no_site    | 7.24 ms                                                                | 7.23 ms: 1.00x faster                                  |
| raytrace                  | 262 ms                                                                 | 264 ms: 1.01x slower                                   |
| xml_etree_generate        | 76.9 ms                                                                | 77.4 ms: 1.01x slower                                  |
| xml_etree_process         | 53.3 ms                                                                | 53.6 ms: 1.01x slower                                  |
| sqlglot_v2_transpile      | 1.52 ms                                                                | 1.54 ms: 1.01x slower                                  |
| sqlglot_v2_parse          | 1.22 ms                                                                | 1.23 ms: 1.01x slower                                  |
| sympy_integrate           | 21.0 ms                                                                | 21.2 ms: 1.01x slower                                  |
| sympy_sum                 | 173 ms                                                                 | 175 ms: 1.01x slower                                   |
| json_loads                | 28.6 us                                                                | 28.8 us: 1.01x slower                                  |
| scimark_sparse_mat_mult   | 4.17 ms                                                                | 4.23 ms: 1.01x slower                                  |
| deltablue                 | 2.83 ms                                                                | 2.87 ms: 1.02x slower                                  |
| spectral_norm             | 83.2 ms                                                                | 84.5 ms: 1.02x slower                                  |
| genshi_xml                | 55.2 ms                                                                | 56.1 ms: 1.02x slower                                  |
| logging_silent            | 83.6 ns                                                                | 85.3 ns: 1.02x slower                                  |
| scimark_sor               | 96.7 ms                                                                | 98.6 ms: 1.02x slower                                  |
| django_template           | 34.4 ms                                                                | 35.1 ms: 1.02x slower                                  |
| coroutines                | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                  |
| pprint_pformat            | 1.39 sec                                                               | 1.45 sec: 1.04x slower                                 |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (45): async_tree_none_tg, async_tree_cpu_io_mixed_tg, sphinx, float, tomli_loads, mdp, pyflate, genshi_text, pathlib, pickle_pure_python, coverage, deepcopy_memo, asyncio_websockets, richards, crypto_pyaes, sympy_expand, async_tree_io, 2to3, chaos, bench_thread_pool, xml_etree_iterparse, subparsers, gc_traversal, sqlglot_v2_optimize, scimark_lu, sqlglot_v2_normalize, many_optionals, sympy_str, regex_compile, sqlite_synth, hexiom, html5lib, json, generators, go, pycparser, async_tree_memoization, pylint, typing_runtime_protocols, async_tree_none, fannkuch, unpickle_pure_python, nqueens, richards_super, pprint_safe_repr
Ignored benchmarks (1) of results/bm-20251124-3.15.0a2+-dc62b62-JIT/bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62.json: docutils

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 76.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x