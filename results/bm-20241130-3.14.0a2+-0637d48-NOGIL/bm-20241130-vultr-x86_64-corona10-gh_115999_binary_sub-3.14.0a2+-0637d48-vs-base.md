# Results vs. base

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 0637d48
- commit date: 2024-11-30
- overall geometric mean: 1.012x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 382 ms                                                                 | 377 ms: 1.01x faster                                                     |
| html5lib       | 103 ms                                                                 | 101 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 637 ms                                                                 | 628 ms: 1.02x faster                                                     |
| async_tree_io              | 894 ms                                                                 | 886 ms: 1.01x faster                                                     |
| async_tree_none            | 402 ms                                                                 | 399 ms: 1.01x faster                                                     |
| coroutines                 | 27.8 ms                                                                | 28.1 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_memoization, async_generators, async_tree_io_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 143 ms                                                                 | 134 ms: 1.07x faster                                                     |
| float          | 143 ms                                                                 | 141 ms: 1.02x faster                                                     |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 196 ms                                                                 | 193 ms: 1.01x faster                                                     |
| regex_v8       | 24.8 ms                                                                | 24.6 ms: 1.01x faster                                                    |
| regex_effbot   | 2.89 ms                                                                | 2.87 ms: 1.01x faster                                                    |
| regex_dna      | 181 ms                                                                 | 187 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.93 sec                                                               | 2.72 sec: 1.08x faster                                                   |
| pickle_pure_python   | 556 us                                                                 | 547 us: 1.02x faster                                                     |
| unpickle_pure_python | 378 us                                                                 | 372 us: 1.02x faster                                                     |
| json_dumps           | 14.5 ms                                                                | 14.3 ms: 1.01x faster                                                    |
| xml_etree_generate   | 103 ms                                                                 | 102 ms: 1.01x faster                                                     |
| xml_etree_process    | 82.7 ms                                                                | 82.2 ms: 1.01x faster                                                    |
| json_loads           | 27.9 us                                                                | 28.3 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                                | 66.9 ms: 1.02x faster                                                    |
| genshi_text     | 34.3 ms                                                                | 33.9 ms: 1.01x faster                                                    |
| mako            | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                    |
| django_template | 55.1 ms                                                                | 55.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| crypto_pyaes               | 104 ms                                                                 | 95.2 ms: 1.09x faster                                                    |
| tomli_loads                | 2.93 sec                                                               | 2.72 sec: 1.08x faster                                                   |
| nbody                      | 143 ms                                                                 | 134 ms: 1.07x faster                                                     |
| hexiom                     | 11.5 ms                                                                | 10.8 ms: 1.06x faster                                                    |
| chaos                      | 116 ms                                                                 | 109 ms: 1.06x faster                                                     |
| fannkuch                   | 534 ms                                                                 | 505 ms: 1.06x faster                                                     |
| richards_super             | 104 ms                                                                 | 98.4 ms: 1.06x faster                                                    |
| nqueens                    | 107 ms                                                                 | 101 ms: 1.05x faster                                                     |
| scimark_lu                 | 203 ms                                                                 | 194 ms: 1.05x faster                                                     |
| logging_silent             | 201 ns                                                                 | 193 ns: 1.04x faster                                                     |
| scimark_monte_carlo        | 124 ms                                                                 | 120 ms: 1.04x faster                                                     |
| go                         | 287 ms                                                                 | 276 ms: 1.04x faster                                                     |
| raytrace                   | 622 ms                                                                 | 601 ms: 1.03x faster                                                     |
| pyflate                    | 736 ms                                                                 | 713 ms: 1.03x faster                                                     |
| sqlglot_parse              | 2.70 ms                                                                | 2.62 ms: 1.03x faster                                                    |
| richards                   | 85.6 ms                                                                | 83.2 ms: 1.03x faster                                                    |
| sqlglot_transpile          | 3.11 ms                                                                | 3.03 ms: 1.03x faster                                                    |
| deltablue                  | 8.89 ms                                                                | 8.66 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult    | 5.82 ms                                                                | 5.69 ms: 1.02x faster                                                    |
| generators                 | 39.2 ms                                                                | 38.4 ms: 1.02x faster                                                    |
| genshi_xml                 | 68.3 ms                                                                | 66.9 ms: 1.02x faster                                                    |
| html5lib                   | 103 ms                                                                 | 101 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 5.56 sec                                                               | 5.45 sec: 1.02x faster                                                   |
| pickle_pure_python         | 556 us                                                                 | 547 us: 1.02x faster                                                     |
| float                      | 143 ms                                                                 | 141 ms: 1.02x faster                                                     |
| unpickle_pure_python       | 378 us                                                                 | 372 us: 1.02x faster                                                     |
| deepcopy_memo              | 45.8 us                                                                | 45.1 us: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 637 ms                                                                 | 628 ms: 1.02x faster                                                     |
| regex_compile              | 196 ms                                                                 | 193 ms: 1.01x faster                                                     |
| deepcopy                   | 355 us                                                                 | 350 us: 1.01x faster                                                     |
| meteor_contest             | 136 ms                                                                 | 134 ms: 1.01x faster                                                     |
| telco                      | 8.95 ms                                                                | 8.84 ms: 1.01x faster                                                    |
| 2to3                       | 382 ms                                                                 | 377 ms: 1.01x faster                                                     |
| many_optionals             | 1.38 ms                                                                | 1.36 ms: 1.01x faster                                                    |
| genshi_text                | 34.3 ms                                                                | 33.9 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.35 us                                                                | 2.32 us: 1.01x faster                                                    |
| dulwich_log                | 100.0 ms                                                               | 98.9 ms: 1.01x faster                                                    |
| regex_v8                   | 24.8 ms                                                                | 24.6 ms: 1.01x faster                                                    |
| scimark_sor                | 243 ms                                                                 | 241 ms: 1.01x faster                                                     |
| coverage                   | 103 ms                                                                 | 102 ms: 1.01x faster                                                     |
| regex_effbot               | 2.89 ms                                                                | 2.87 ms: 1.01x faster                                                    |
| async_tree_io              | 894 ms                                                                 | 886 ms: 1.01x faster                                                     |
| sympy_integrate            | 31.0 ms                                                                | 30.7 ms: 1.01x faster                                                    |
| json_dumps                 | 14.5 ms                                                                | 14.3 ms: 1.01x faster                                                    |
| mdp                        | 2.93 sec                                                               | 2.90 sec: 1.01x faster                                                   |
| xml_etree_generate         | 103 ms                                                                 | 102 ms: 1.01x faster                                                     |
| pprint_pformat             | 2.23 sec                                                               | 2.22 sec: 1.01x faster                                                   |
| k_core                     | 2.47 sec                                                               | 2.45 sec: 1.01x faster                                                   |
| async_tree_none            | 402 ms                                                                 | 399 ms: 1.01x faster                                                     |
| xml_etree_process          | 82.7 ms                                                                | 82.2 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 1.08 sec                                                               | 1.07 sec: 1.00x faster                                                   |
| pycparser                  | 1.60 sec                                                               | 1.59 sec: 1.00x faster                                                   |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| shortest_path              | 566 ms                                                                 | 567 ms: 1.00x slower                                                     |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                    |
| bench_thread_pool          | 3.38 ms                                                                | 3.40 ms: 1.00x slower                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                    |
| pathlib                    | 20.8 ms                                                                | 20.9 ms: 1.01x slower                                                    |
| connected_components       | 514 ms                                                                 | 518 ms: 1.01x slower                                                     |
| mako                       | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 213 us                                                                 | 215 us: 1.01x slower                                                     |
| scimark_fft                | 400 ms                                                                 | 404 ms: 1.01x slower                                                     |
| django_template            | 55.1 ms                                                                | 55.7 ms: 1.01x slower                                                    |
| spectral_norm              | 130 ms                                                                 | 132 ms: 1.01x slower                                                     |
| json_loads                 | 27.9 us                                                                | 28.3 us: 1.01x slower                                                    |
| coroutines                 | 27.8 ms                                                                | 28.1 ms: 1.01x slower                                                    |
| regex_dna                  | 181 ms                                                                 | 187 ms: 1.03x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (27): docutils, async_tree_cpu_io_mixed, async_tree_memoization, json, async_generators, async_tree_io_tg, logging_format, xml_etree_iterparse, sphinx, subparsers, async_tree_memoization_tg, sqlglot_optimize, sympy_str, sympy_expand, pylint, comprehensions, thrift, sympy_sum, logging_simple, bench_mp_pool, gc_traversal, deepcopy_reduce, sqlglot_normalize, create_gc_cycles, asyncio_websockets, async_tree_none_tg, xml_etree_parse

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x