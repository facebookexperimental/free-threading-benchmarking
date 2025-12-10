# Results vs. base

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: a2c45c6
- commit date: 2025-12-09
- overall geometric mean: 1.013x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 277 ms: 1.01x faster                                                     |
| docutils       | 2.77 sec                                                               | 2.70 sec: 1.02x faster                                                   |
| html5lib       | 68.7 ms                                                                | 65.9 ms: 1.04x faster                                                    |
| sphinx         | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg | 335 ms                                                                 | 329 ms: 1.02x faster                                                     |
| async_tree_none           | 292 ms                                                                 | 287 ms: 1.02x faster                                                     |
| coroutines                | 23.9 ms                                                                | 23.9 ms: 1.00x faster                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (8): async_tree_io, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization, asyncio_websockets, async_generators, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 126 ms                                                                 | 121 ms: 1.04x faster                                                     |
| float          | 73.8 ms                                                                | 72.3 ms: 1.02x faster                                                    |
| pidigits       | 192 ms                                                                 | 215 ms: 1.12x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                 | 141 ms: 1.01x faster                                                     |
| regex_v8       | 21.1 ms                                                                | 22.1 ms: 1.05x slower                                                    |
| regex_dna      | 170 ms                                                                 | 181 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 69.8 ms                                                                | 68.1 ms: 1.02x faster                                                    |
| tomli_loads          | 2.34 sec                                                               | 2.29 sec: 1.02x faster                                                   |
| xml_etree_iterparse  | 95.6 ms                                                                | 93.5 ms: 1.02x faster                                                    |
| pickle_pure_python   | 337 us                                                                 | 330 us: 1.02x faster                                                     |
| json_dumps           | 11.0 ms                                                                | 10.7 ms: 1.02x faster                                                    |
| unpickle_pure_python | 237 us                                                                 | 233 us: 1.02x faster                                                     |
| xml_etree_generate   | 96.9 ms                                                                | 95.3 ms: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| python_startup_no_site | 9.78 ms                                                                | 9.70 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 16.1 ms                                                                | 15.5 ms: 1.04x faster                                                    |
| genshi_xml     | 58.6 ms                                                                | 56.9 ms: 1.03x faster                                                    |
| genshi_text    | 26.7 ms                                                                | 26.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                 | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_sparse_mat_mult   | 5.51 ms                                                                | 5.25 ms: 1.05x faster                                                    |
| generators                | 31.8 ms                                                                | 30.3 ms: 1.05x faster                                                    |
| deepcopy_reduce           | 3.03 us                                                                | 2.90 us: 1.05x faster                                                    |
| hexiom                    | 6.51 ms                                                                | 6.23 ms: 1.05x faster                                                    |
| scimark_lu                | 134 ms                                                                 | 128 ms: 1.04x faster                                                     |
| html5lib                  | 68.7 ms                                                                | 65.9 ms: 1.04x faster                                                    |
| nbody                     | 126 ms                                                                 | 121 ms: 1.04x faster                                                     |
| comprehensions            | 18.1 us                                                                | 17.4 us: 1.04x faster                                                    |
| scimark_monte_carlo       | 79.7 ms                                                                | 76.7 ms: 1.04x faster                                                    |
| deepcopy                  | 283 us                                                                 | 272 us: 1.04x faster                                                     |
| mako                      | 16.1 ms                                                                | 15.5 ms: 1.04x faster                                                    |
| go                        | 122 ms                                                                 | 118 ms: 1.04x faster                                                     |
| spectral_norm             | 112 ms                                                                 | 108 ms: 1.04x faster                                                     |
| scimark_sor               | 124 ms                                                                 | 120 ms: 1.03x faster                                                     |
| bpe_tokeniser             | 4.44 sec                                                               | 4.30 sec: 1.03x faster                                                   |
| chaos                     | 63.5 ms                                                                | 61.7 ms: 1.03x faster                                                    |
| logging_silent            | 106 ns                                                                 | 103 ns: 1.03x faster                                                     |
| genshi_xml                | 58.6 ms                                                                | 56.9 ms: 1.03x faster                                                    |
| many_optionals            | 1.03 ms                                                                | 1.00 ms: 1.03x faster                                                    |
| logging_simple            | 6.96 us                                                                | 6.77 us: 1.03x faster                                                    |
| pyflate                   | 463 ms                                                                 | 451 ms: 1.03x faster                                                     |
| thrift                    | 888 us                                                                 | 865 us: 1.03x faster                                                     |
| docutils                  | 2.77 sec                                                               | 2.70 sec: 1.02x faster                                                   |
| xml_etree_process         | 69.8 ms                                                                | 68.1 ms: 1.02x faster                                                    |
| tomli_loads               | 2.34 sec                                                               | 2.29 sec: 1.02x faster                                                   |
| xml_etree_iterparse       | 95.6 ms                                                                | 93.5 ms: 1.02x faster                                                    |
| sympy_str                 | 313 ms                                                                 | 306 ms: 1.02x faster                                                     |
| sqlglot_v2_transpile      | 1.76 ms                                                                | 1.73 ms: 1.02x faster                                                    |
| float                     | 73.8 ms                                                                | 72.3 ms: 1.02x faster                                                    |
| pickle_pure_python        | 337 us                                                                 | 330 us: 1.02x faster                                                     |
| json_dumps                | 11.0 ms                                                                | 10.7 ms: 1.02x faster                                                    |
| richards_super            | 59.7 ms                                                                | 58.6 ms: 1.02x faster                                                    |
| sphinx                    | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                                   |
| fannkuch                  | 465 ms                                                                 | 456 ms: 1.02x faster                                                     |
| sqlglot_v2_normalize      | 116 ms                                                                 | 114 ms: 1.02x faster                                                     |
| subparsers                | 10.3 ms                                                                | 10.1 ms: 1.02x faster                                                    |
| pprint_safe_repr          | 782 ms                                                                 | 767 ms: 1.02x faster                                                     |
| async_tree_memoization_tg | 335 ms                                                                 | 329 ms: 1.02x faster                                                     |
| unpickle_pure_python      | 237 us                                                                 | 233 us: 1.02x faster                                                     |
| richards                  | 52.0 ms                                                                | 51.1 ms: 1.02x faster                                                    |
| deepcopy_memo             | 30.8 us                                                                | 30.3 us: 1.02x faster                                                    |
| mdp                       | 1.32 sec                                                               | 1.30 sec: 1.02x faster                                                   |
| logging_format            | 7.89 us                                                                | 7.76 us: 1.02x faster                                                    |
| async_tree_none           | 292 ms                                                                 | 287 ms: 1.02x faster                                                     |
| xml_etree_generate        | 96.9 ms                                                                | 95.3 ms: 1.02x faster                                                    |
| sqlglot_v2_parse          | 1.47 ms                                                                | 1.45 ms: 1.02x faster                                                    |
| sqlglot_v2_optimize       | 58.6 ms                                                                | 57.7 ms: 1.02x faster                                                    |
| crypto_pyaes              | 86.6 ms                                                                | 85.3 ms: 1.02x faster                                                    |
| genshi_text               | 26.7 ms                                                                | 26.3 ms: 1.01x faster                                                    |
| raytrace                  | 300 ms                                                                 | 296 ms: 1.01x faster                                                     |
| pprint_pformat            | 1.61 sec                                                               | 1.59 sec: 1.01x faster                                                   |
| shortest_path             | 528 ms                                                                 | 521 ms: 1.01x faster                                                     |
| regex_compile             | 143 ms                                                                 | 141 ms: 1.01x faster                                                     |
| create_gc_cycles          | 1.50 ms                                                                | 1.48 ms: 1.01x faster                                                    |
| meteor_contest            | 120 ms                                                                 | 119 ms: 1.01x faster                                                     |
| sympy_integrate           | 21.9 ms                                                                | 21.6 ms: 1.01x faster                                                    |
| telco                     | 177 ms                                                                 | 175 ms: 1.01x faster                                                     |
| 2to3                      | 280 ms                                                                 | 277 ms: 1.01x faster                                                     |
| nqueens                   | 88.4 ms                                                                | 87.5 ms: 1.01x faster                                                    |
| coverage                  | 112 ms                                                                 | 111 ms: 1.01x faster                                                     |
| python_startup            | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| dulwich_log               | 72.5 ms                                                                | 71.9 ms: 1.01x faster                                                    |
| python_startup_no_site    | 9.78 ms                                                                | 9.70 ms: 1.01x faster                                                    |
| sympy_sum                 | 177 ms                                                                 | 176 ms: 1.01x faster                                                     |
| pycparser                 | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                   |
| scimark_fft               | 346 ms                                                                 | 344 ms: 1.01x faster                                                     |
| pathlib                   | 17.7 ms                                                                | 17.7 ms: 1.01x faster                                                    |
| coroutines                | 23.9 ms                                                                | 23.9 ms: 1.00x faster                                                    |
| k_core                    | 2.20 sec                                                               | 2.21 sec: 1.00x slower                                                   |
| deltablue                 | 3.70 ms                                                                | 3.77 ms: 1.02x slower                                                    |
| sqlite_synth              | 2.04 us                                                                | 2.09 us: 1.02x slower                                                    |
| regex_v8                  | 21.1 ms                                                                | 22.1 ms: 1.05x slower                                                    |
| regex_dna                 | 170 ms                                                                 | 181 ms: 1.06x slower                                                     |
| pidigits                  | 192 ms                                                                 | 215 ms: 1.12x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (20): pylint, async_tree_io, async_tree_none_tg, typing_runtime_protocols, async_tree_io_tg, sympy_expand, bench_thread_pool, async_tree_cpu_io_mixed, django_template, async_tree_memoization, gc_traversal, xml_etree_parse, connected_components, bench_mp_pool, asyncio_websockets, json_loads, async_generators, json, regex_effbot, async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x