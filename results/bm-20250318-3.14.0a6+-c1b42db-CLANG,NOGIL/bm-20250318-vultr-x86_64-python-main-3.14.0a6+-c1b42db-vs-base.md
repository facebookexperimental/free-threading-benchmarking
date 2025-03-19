# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c1b42db
- commit date: 2025-03-18
- overall geometric mean: 1.003x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 275 ms: 1.01x faster                                   |
| html5lib       | 65.9 ms                                                                | 65.3 ms: 1.01x faster                                  |
| sphinx         | 1.04 sec                                                               | 1.04 sec: 1.00x faster                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| coroutines             | 20.5 ms                                                                | 20.2 ms: 1.01x faster                                  |
| async_tree_none        | 254 ms                                                                 | 252 ms: 1.01x faster                                   |
| async_generators       | 327 ms                                                                 | 324 ms: 1.01x faster                                   |
| async_tree_memoization | 312 ms                                                                 | 310 ms: 1.01x faster                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 68.2 ms                                                                | 68.0 ms: 1.00x faster                                  |
| pidigits       | 187 ms                                                                 | 186 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 206 ms                                                                 | 202 ms: 1.02x faster                                   |
| regex_compile  | 141 ms                                                                 | 138 ms: 1.02x faster                                   |
| regex_effbot   | 3.31 ms                                                                | 3.26 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_pure_python | 228 us                                                                 | 224 us: 1.02x faster                                   |
| json_dumps           | 12.6 ms                                                                | 12.5 ms: 1.01x faster                                  |
| xml_etree_iterparse  | 84.8 ms                                                                | 84.3 ms: 1.01x faster                                  |
| xml_etree_process    | 60.3 ms                                                                | 60.0 ms: 1.00x faster                                  |
| xml_etree_generate   | 85.3 ms                                                                | 85.1 ms: 1.00x faster                                  |
| pickle_pure_python   | 322 us                                                                 | 325 us: 1.01x slower                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup | 15.5 ms                                                                | 15.5 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| mako           | 14.9 ms                                                                | 14.8 ms: 1.01x faster                                  |
| genshi_text    | 23.9 ms                                                                | 24.2 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6+-f819900 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| coverage                 | 89.2 ms                                                                | 85.3 ms: 1.05x faster                                  |
| richards                 | 47.8 ms                                                                | 46.6 ms: 1.03x faster                                  |
| regex_dna                | 206 ms                                                                 | 202 ms: 1.02x faster                                   |
| richards_super           | 56.2 ms                                                                | 55.0 ms: 1.02x faster                                  |
| regex_compile            | 141 ms                                                                 | 138 ms: 1.02x faster                                   |
| sqlalchemy_imperative    | 22.9 ms                                                                | 22.5 ms: 1.02x faster                                  |
| raytrace                 | 288 ms                                                                 | 283 ms: 1.02x faster                                   |
| unpickle_pure_python     | 228 us                                                                 | 224 us: 1.02x faster                                   |
| regex_effbot             | 3.31 ms                                                                | 3.26 ms: 1.02x faster                                  |
| sqlglot_v2_parse         | 1.42 ms                                                                | 1.39 ms: 1.02x faster                                  |
| sqlglot_v2_transpile     | 1.72 ms                                                                | 1.69 ms: 1.02x faster                                  |
| telco                    | 8.14 ms                                                                | 8.02 ms: 1.02x faster                                  |
| pyflate                  | 449 ms                                                                 | 443 ms: 1.01x faster                                   |
| go                       | 124 ms                                                                 | 122 ms: 1.01x faster                                   |
| coroutines               | 20.5 ms                                                                | 20.2 ms: 1.01x faster                                  |
| scimark_sor              | 113 ms                                                                 | 112 ms: 1.01x faster                                   |
| json                     | 5.24 ms                                                                | 5.18 ms: 1.01x faster                                  |
| crypto_pyaes             | 80.4 ms                                                                | 79.5 ms: 1.01x faster                                  |
| scimark_monte_carlo      | 70.0 ms                                                                | 69.3 ms: 1.01x faster                                  |
| sympy_integrate          | 22.2 ms                                                                | 22.0 ms: 1.01x faster                                  |
| generators               | 27.4 ms                                                                | 27.1 ms: 1.01x faster                                  |
| sympy_str                | 307 ms                                                                 | 304 ms: 1.01x faster                                   |
| json_dumps               | 12.6 ms                                                                | 12.5 ms: 1.01x faster                                  |
| html5lib                 | 65.9 ms                                                                | 65.3 ms: 1.01x faster                                  |
| typing_runtime_protocols | 174 us                                                                 | 172 us: 1.01x faster                                   |
| sympy_sum                | 173 ms                                                                 | 171 ms: 1.01x faster                                   |
| async_tree_none          | 254 ms                                                                 | 252 ms: 1.01x faster                                   |
| async_generators         | 327 ms                                                                 | 324 ms: 1.01x faster                                   |
| 2to3                     | 277 ms                                                                 | 275 ms: 1.01x faster                                   |
| gc_traversal             | 1.96 ms                                                                | 1.94 ms: 1.01x faster                                  |
| mako                     | 14.9 ms                                                                | 14.8 ms: 1.01x faster                                  |
| pprint_safe_repr         | 775 ms                                                                 | 769 ms: 1.01x faster                                   |
| sympy_expand             | 504 ms                                                                 | 500 ms: 1.01x faster                                   |
| deepcopy_memo            | 34.0 us                                                                | 33.7 us: 1.01x faster                                  |
| async_tree_memoization   | 312 ms                                                                 | 310 ms: 1.01x faster                                   |
| sqlalchemy_declarative   | 150 ms                                                                 | 149 ms: 1.01x faster                                   |
| chaos                    | 61.1 ms                                                                | 60.7 ms: 1.01x faster                                  |
| hexiom                   | 6.61 ms                                                                | 6.57 ms: 1.01x faster                                  |
| xml_etree_iterparse      | 84.8 ms                                                                | 84.3 ms: 1.01x faster                                  |
| pathlib                  | 19.1 ms                                                                | 19.0 ms: 1.01x faster                                  |
| deepcopy_reduce          | 2.78 us                                                                | 2.77 us: 1.01x faster                                  |
| create_gc_cycles         | 1.35 ms                                                                | 1.34 ms: 1.01x faster                                  |
| meteor_contest           | 123 ms                                                                 | 122 ms: 1.00x faster                                   |
| fannkuch                 | 437 ms                                                                 | 435 ms: 1.00x faster                                   |
| sphinx                   | 1.04 sec                                                               | 1.04 sec: 1.00x faster                                 |
| xml_etree_process        | 60.3 ms                                                                | 60.0 ms: 1.00x faster                                  |
| xml_etree_generate       | 85.3 ms                                                                | 85.1 ms: 1.00x faster                                  |
| sqlglot_v2_normalize     | 106 ms                                                                 | 106 ms: 1.00x faster                                   |
| float                    | 68.2 ms                                                                | 68.0 ms: 1.00x faster                                  |
| logging_silent           | 87.2 ns                                                                | 87.0 ns: 1.00x faster                                  |
| pidigits                 | 187 ms                                                                 | 186 ms: 1.00x faster                                   |
| python_startup           | 15.5 ms                                                                | 15.5 ms: 1.00x faster                                  |
| bench_thread_pool        | 3.10 ms                                                                | 3.11 ms: 1.00x slower                                  |
| nqueens                  | 84.5 ms                                                                | 84.7 ms: 1.00x slower                                  |
| bpe_tokeniser            | 4.38 sec                                                               | 4.39 sec: 1.00x slower                                 |
| k_core                   | 2.22 sec                                                               | 2.23 sec: 1.00x slower                                 |
| comprehensions           | 17.5 us                                                                | 17.6 us: 1.01x slower                                  |
| scimark_lu               | 115 ms                                                                 | 115 ms: 1.01x slower                                   |
| pickle_pure_python       | 322 us                                                                 | 325 us: 1.01x slower                                   |
| genshi_text              | 23.9 ms                                                                | 24.2 ms: 1.01x slower                                  |
| thrift                   | 821 us                                                                 | 832 us: 1.01x slower                                   |
| logging_format           | 7.30 us                                                                | 7.41 us: 1.02x slower                                  |
| spectral_norm            | 94.6 ms                                                                | 96.1 ms: 1.02x slower                                  |
| sqlite_synth             | 1.96 us                                                                | 2.02 us: 1.03x slower                                  |
| scimark_fft              | 329 ms                                                                 | 341 ms: 1.04x slower                                   |
| mdp                      | 2.62 sec                                                               | 2.74 sec: 1.05x slower                                 |
| scimark_sparse_mat_mult  | 4.65 ms                                                                | 4.92 ms: 1.06x slower                                  |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (29): async_tree_io_tg, pylint, connected_components, docutils, shortest_path, bench_mp_pool, deltablue, django_template, deepcopy, async_tree_memoization_tg, many_optionals, pprint_pformat, dulwich_log, subparsers, python_startup_no_site, asyncio_websockets, sqlglot_v2_optimize, nbody, xml_etree_parse, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, regex_v8, async_tree_io, json_loads, tomli_loads, pycparser, genshi_xml, logging_simple, async_tree_none_tg

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x