# Results vs. base

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: d3f79e5
- commit date: 2025-04-17
- overall geometric mean: 1.001x faster
- HPT reliability: 71.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 278 ms: 1.01x faster                                                     |
| docutils       | 2.69 sec                                                               | 2.68 sec: 1.00x faster                                                   |
| html5lib       | 67.6 ms                                                                | 66.4 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg | 286 ms                                                                 | 282 ms: 1.01x faster                                                     |
| async_tree_io             | 547 ms                                                                 | 543 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed   | 502 ms                                                                 | 505 ms: 1.01x slower                                                     |
| coroutines                | 22.4 ms                                                                | 22.9 ms: 1.02x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_none, async_generators, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                    |
| pidigits       | 190 ms                                                                 | 193 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.97 ms                                                                | 2.86 ms: 1.04x faster                                                    |
| regex_dna      | 191 ms                                                                 | 187 ms: 1.02x faster                                                     |
| regex_v8       | 21.3 ms                                                                | 21.7 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 227 us                                                                 | 225 us: 1.01x faster                                                     |
| tomli_loads          | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                   |
| xml_etree_iterparse  | 87.4 ms                                                                | 86.8 ms: 1.01x faster                                                    |
| json_dumps           | 12.7 ms                                                                | 12.6 ms: 1.01x faster                                                    |
| pickle_pure_python   | 326 us                                                                 | 325 us: 1.00x faster                                                     |
| xml_etree_process    | 66.1 ms                                                                | 66.4 ms: 1.00x slower                                                    |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 15.5 ms                                                                | 15.2 ms: 1.02x faster                                                    |
| django_template | 40.1 ms                                                                | 39.7 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7+-e42bda9 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_sor               | 122 ms                                                                 | 117 ms: 1.04x faster                                                     |
| regex_effbot              | 2.97 ms                                                                | 2.86 ms: 1.04x faster                                                    |
| pyflate                   | 469 ms                                                                 | 455 ms: 1.03x faster                                                     |
| logging_silent            | 105 ns                                                                 | 102 ns: 1.03x faster                                                     |
| fannkuch                  | 460 ms                                                                 | 451 ms: 1.02x faster                                                     |
| deepcopy_reduce           | 3.01 us                                                                | 2.95 us: 1.02x faster                                                    |
| coverage                  | 111 ms                                                                 | 109 ms: 1.02x faster                                                     |
| comprehensions            | 19.5 us                                                                | 19.1 us: 1.02x faster                                                    |
| regex_dna                 | 191 ms                                                                 | 187 ms: 1.02x faster                                                     |
| html5lib                  | 67.6 ms                                                                | 66.4 ms: 1.02x faster                                                    |
| mako                      | 15.5 ms                                                                | 15.2 ms: 1.02x faster                                                    |
| telco                     | 8.41 ms                                                                | 8.27 ms: 1.02x faster                                                    |
| hexiom                    | 6.72 ms                                                                | 6.63 ms: 1.01x faster                                                    |
| deepcopy                  | 293 us                                                                 | 289 us: 1.01x faster                                                     |
| sqlglot_v2_transpile      | 1.78 ms                                                                | 1.75 ms: 1.01x faster                                                    |
| async_tree_memoization_tg | 286 ms                                                                 | 282 ms: 1.01x faster                                                     |
| deepcopy_memo             | 35.0 us                                                                | 34.6 us: 1.01x faster                                                    |
| nqueens                   | 87.7 ms                                                                | 86.7 ms: 1.01x faster                                                    |
| unpickle_pure_python      | 227 us                                                                 | 225 us: 1.01x faster                                                     |
| django_template           | 40.1 ms                                                                | 39.7 ms: 1.01x faster                                                    |
| json                      | 5.21 ms                                                                | 5.16 ms: 1.01x faster                                                    |
| tomli_loads               | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                   |
| subparsers                | 24.5 ms                                                                | 24.3 ms: 1.01x faster                                                    |
| async_tree_io             | 547 ms                                                                 | 543 ms: 1.01x faster                                                     |
| python_startup            | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| gc_traversal              | 1.77 ms                                                                | 1.76 ms: 1.01x faster                                                    |
| xml_etree_iterparse       | 87.4 ms                                                                | 86.8 ms: 1.01x faster                                                    |
| bench_mp_pool             | 95.6 ms                                                                | 94.9 ms: 1.01x faster                                                    |
| python_startup_no_site    | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| go                        | 125 ms                                                                 | 124 ms: 1.01x faster                                                     |
| dulwich_log               | 70.7 ms                                                                | 70.2 ms: 1.01x faster                                                    |
| create_gc_cycles          | 1.35 ms                                                                | 1.34 ms: 1.01x faster                                                    |
| float                     | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                    |
| generators                | 30.8 ms                                                                | 30.6 ms: 1.01x faster                                                    |
| 2to3                      | 280 ms                                                                 | 278 ms: 1.01x faster                                                     |
| json_dumps                | 12.7 ms                                                                | 12.6 ms: 1.01x faster                                                    |
| pickle_pure_python        | 326 us                                                                 | 325 us: 1.00x faster                                                     |
| docutils                  | 2.69 sec                                                               | 2.68 sec: 1.00x faster                                                   |
| pprint_safe_repr          | 771 ms                                                                 | 773 ms: 1.00x slower                                                     |
| sympy_integrate           | 22.0 ms                                                                | 22.0 ms: 1.00x slower                                                    |
| bench_thread_pool         | 3.12 ms                                                                | 3.14 ms: 1.00x slower                                                    |
| mdp                       | 1.30 sec                                                               | 1.31 sec: 1.00x slower                                                   |
| pathlib                   | 19.1 ms                                                                | 19.2 ms: 1.00x slower                                                    |
| xml_etree_process         | 66.1 ms                                                                | 66.4 ms: 1.00x slower                                                    |
| chaos                     | 61.0 ms                                                                | 61.3 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed   | 502 ms                                                                 | 505 ms: 1.01x slower                                                     |
| scimark_monte_carlo       | 73.3 ms                                                                | 73.7 ms: 1.01x slower                                                    |
| sqlalchemy_declarative    | 153 ms                                                                 | 154 ms: 1.01x slower                                                     |
| bpe_tokeniser             | 4.48 sec                                                               | 4.51 sec: 1.01x slower                                                   |
| xml_etree_parse           | 128 ms                                                                 | 129 ms: 1.01x slower                                                     |
| logging_simple            | 6.89 us                                                                | 6.97 us: 1.01x slower                                                    |
| typing_runtime_protocols  | 191 us                                                                 | 193 us: 1.01x slower                                                     |
| pycparser                 | 1.11 sec                                                               | 1.12 sec: 1.01x slower                                                   |
| sympy_expand              | 524 ms                                                                 | 531 ms: 1.01x slower                                                     |
| pidigits                  | 190 ms                                                                 | 193 ms: 1.01x slower                                                     |
| richards_super            | 57.6 ms                                                                | 58.5 ms: 1.02x slower                                                    |
| crypto_pyaes              | 81.7 ms                                                                | 83.1 ms: 1.02x slower                                                    |
| richards                  | 50.0 ms                                                                | 50.8 ms: 1.02x slower                                                    |
| deltablue                 | 3.52 ms                                                                | 3.59 ms: 1.02x slower                                                    |
| coroutines                | 22.4 ms                                                                | 22.9 ms: 1.02x slower                                                    |
| regex_v8                  | 21.3 ms                                                                | 21.7 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult   | 4.75 ms                                                                | 4.94 ms: 1.04x slower                                                    |
| scimark_fft               | 339 ms                                                                 | 353 ms: 1.04x slower                                                     |
| spectral_norm             | 99.9 ms                                                                | 104 ms: 1.05x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (31): meteor_contest, async_tree_io_tg, async_tree_none_tg, scimark_lu, async_tree_memoization, async_tree_none, shortest_path, async_generators, regex_compile, sphinx, many_optionals, json_loads, raytrace, sqlglot_v2_parse, sqlglot_v2_normalize, k_core, pprint_pformat, nbody, asyncio_websockets, sqlglot_v2_optimize, connected_components, xml_etree_generate, sympy_str, sqlalchemy_imperative, sympy_sum, async_tree_cpu_io_mixed_tg, pylint, genshi_text, logging_format, genshi_xml, sqlite_synth

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 71.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x