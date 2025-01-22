# Results vs. base

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.005x faster
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 252 ms: 1.02x faster                                                  |
| docutils       | 2.60 sec                                                               | 2.55 sec: 1.02x faster                                                |
| sphinx         | 993 ms                                                                 | 983 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg | 260 ms                                                                 | 257 ms: 1.01x faster                                                  |
| coroutines         | 22.0 ms                                                                | 22.1 ms: 1.00x slower                                                 |
| async_generators   | 322 ms                                                                 | 325 ms: 1.01x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (8): async_tree_io, async_tree_none, async_tree_cpu_io_mixed, async_tree_io_tg, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 90.7 ms                                                                | 89.2 ms: 1.02x faster                                                 |
| float          | 70.9 ms                                                                | 72.4 ms: 1.02x slower                                                 |
| pidigits       | 192 ms                                                                 | 207 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| regex_effbot   | 2.72 ms                                                                | 2.72 ms: 1.00x faster                                                 |
| regex_dna      | 173 ms                                                                 | 174 ms: 1.01x slower                                                  |
| regex_v8       | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 322 us                                                                 | 313 us: 1.03x faster                                                  |
| tomli_loads          | 1.96 sec                                                               | 1.91 sec: 1.03x faster                                                |
| xml_etree_process    | 60.6 ms                                                                | 59.0 ms: 1.03x faster                                                 |
| unpickle_pure_python | 226 us                                                                 | 220 us: 1.03x faster                                                  |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| json_dumps           | 11.4 ms                                                                | 11.3 ms: 1.00x faster                                                 |
| json_loads           | 27.6 us                                                                | 27.9 us: 1.01x slower                                                 |
| xml_etree_generate   | 83.3 ms                                                                | 84.4 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.43 ms                                                                | 7.41 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.4 ms                                                                | 35.5 ms: 1.03x faster                                                 |
| genshi_xml      | 49.9 ms                                                                | 48.8 ms: 1.02x faster                                                 |
| mako            | 11.8 ms                                                                | 12.0 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_simple           | 6.50 us                                                                | 6.17 us: 1.05x faster                                                 |
| pathlib                  | 18.8 ms                                                                | 18.0 ms: 1.05x faster                                                 |
| logging_format           | 7.21 us                                                                | 6.89 us: 1.05x faster                                                 |
| many_optionals           | 1.05 ms                                                                | 1.01 ms: 1.03x faster                                                 |
| pycparser                | 1.14 sec                                                               | 1.11 sec: 1.03x faster                                                |
| pickle_pure_python       | 322 us                                                                 | 313 us: 1.03x faster                                                  |
| scimark_lu               | 112 ms                                                                 | 109 ms: 1.03x faster                                                  |
| tomli_loads              | 1.96 sec                                                               | 1.91 sec: 1.03x faster                                                |
| xml_etree_process        | 60.6 ms                                                                | 59.0 ms: 1.03x faster                                                 |
| django_template          | 36.4 ms                                                                | 35.5 ms: 1.03x faster                                                 |
| unpickle_pure_python     | 226 us                                                                 | 220 us: 1.03x faster                                                  |
| go                       | 118 ms                                                                 | 115 ms: 1.03x faster                                                  |
| fannkuch                 | 374 ms                                                                 | 366 ms: 1.02x faster                                                  |
| sqlalchemy_imperative    | 19.8 ms                                                                | 19.3 ms: 1.02x faster                                                 |
| genshi_xml               | 49.9 ms                                                                | 48.8 ms: 1.02x faster                                                 |
| regex_compile            | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| thrift                   | 749 us                                                                 | 733 us: 1.02x faster                                                  |
| scimark_sparse_mat_mult  | 4.17 ms                                                                | 4.09 ms: 1.02x faster                                                 |
| sympy_sum                | 156 ms                                                                 | 153 ms: 1.02x faster                                                  |
| dulwich_log              | 77.0 ms                                                                | 75.6 ms: 1.02x faster                                                 |
| hexiom                   | 5.90 ms                                                                | 5.79 ms: 1.02x faster                                                 |
| sympy_integrate          | 20.0 ms                                                                | 19.7 ms: 1.02x faster                                                 |
| nbody                    | 90.7 ms                                                                | 89.2 ms: 1.02x faster                                                 |
| docutils                 | 2.60 sec                                                               | 2.55 sec: 1.02x faster                                                |
| sqlglot_optimize         | 52.9 ms                                                                | 52.0 ms: 1.02x faster                                                 |
| 2to3                     | 256 ms                                                                 | 252 ms: 1.02x faster                                                  |
| bpe_tokeniser            | 4.25 sec                                                               | 4.19 sec: 1.02x faster                                                |
| sympy_str                | 275 ms                                                                 | 271 ms: 1.02x faster                                                  |
| sqlalchemy_declarative   | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| sympy_expand             | 463 ms                                                                 | 456 ms: 1.01x faster                                                  |
| subparsers               | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                                 |
| bench_mp_pool            | 89.0 ms                                                                | 87.9 ms: 1.01x faster                                                 |
| sqlglot_normalize        | 105 ms                                                                 | 104 ms: 1.01x faster                                                  |
| async_tree_none_tg       | 260 ms                                                                 | 257 ms: 1.01x faster                                                  |
| sqlite_synth             | 2.21 us                                                                | 2.19 us: 1.01x faster                                                 |
| xml_etree_parse          | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| typing_runtime_protocols | 158 us                                                                 | 156 us: 1.01x faster                                                  |
| crypto_pyaes             | 67.8 ms                                                                | 67.1 ms: 1.01x faster                                                 |
| sphinx                   | 993 ms                                                                 | 983 ms: 1.01x faster                                                  |
| deltablue                | 3.20 ms                                                                | 3.18 ms: 1.01x faster                                                 |
| coverage                 | 80.0 ms                                                                | 79.5 ms: 1.01x faster                                                 |
| raytrace                 | 266 ms                                                                 | 265 ms: 1.01x faster                                                  |
| python_startup           | 14.6 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| deepcopy_reduce          | 2.66 us                                                                | 2.64 us: 1.01x faster                                                 |
| sqlglot_transpile        | 1.56 ms                                                                | 1.55 ms: 1.01x faster                                                 |
| json_dumps               | 11.4 ms                                                                | 11.3 ms: 1.00x faster                                                 |
| python_startup_no_site   | 7.43 ms                                                                | 7.41 ms: 1.00x faster                                                 |
| spectral_norm            | 94.0 ms                                                                | 93.8 ms: 1.00x faster                                                 |
| regex_effbot             | 2.72 ms                                                                | 2.72 ms: 1.00x faster                                                 |
| nqueens                  | 77.9 ms                                                                | 78.2 ms: 1.00x slower                                                 |
| coroutines               | 22.0 ms                                                                | 22.1 ms: 1.00x slower                                                 |
| mdp                      | 2.31 sec                                                               | 2.32 sec: 1.01x slower                                                |
| regex_dna                | 173 ms                                                                 | 174 ms: 1.01x slower                                                  |
| regex_v8                 | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                                 |
| connected_components     | 390 ms                                                                 | 393 ms: 1.01x slower                                                  |
| richards                 | 42.4 ms                                                                | 42.8 ms: 1.01x slower                                                 |
| comprehensions           | 16.6 us                                                                | 16.8 us: 1.01x slower                                                 |
| richards_super           | 48.5 ms                                                                | 49.1 ms: 1.01x slower                                                 |
| scimark_monte_carlo      | 63.0 ms                                                                | 63.7 ms: 1.01x slower                                                 |
| json_loads               | 27.6 us                                                                | 27.9 us: 1.01x slower                                                 |
| mako                     | 11.8 ms                                                                | 12.0 ms: 1.01x slower                                                 |
| async_generators         | 322 ms                                                                 | 325 ms: 1.01x slower                                                  |
| create_gc_cycles         | 1.82 ms                                                                | 1.84 ms: 1.01x slower                                                 |
| xml_etree_generate       | 83.3 ms                                                                | 84.4 ms: 1.01x slower                                                 |
| float                    | 70.9 ms                                                                | 72.4 ms: 1.02x slower                                                 |
| shortest_path            | 427 ms                                                                 | 436 ms: 1.02x slower                                                  |
| scimark_sor              | 113 ms                                                                 | 116 ms: 1.03x slower                                                  |
| gc_traversal             | 4.18 ms                                                                | 4.29 ms: 1.03x slower                                                 |
| logging_silent           | 103 ns                                                                 | 106 ns: 1.03x slower                                                  |
| pyflate                  | 411 ms                                                                 | 428 ms: 1.04x slower                                                  |
| pidigits                 | 192 ms                                                                 | 207 ms: 1.08x slower                                                  |
| generators               | 27.3 ms                                                                | 30.6 ms: 1.12x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (23): pylint, async_tree_io, async_tree_none, telco, scimark_fft, async_tree_cpu_io_mixed, deepcopy, async_tree_io_tg, chaos, bench_thread_pool, sqlglot_parse, genshi_text, xml_etree_iterparse, json, k_core, deepcopy_memo, asyncio_websockets, pprint_safe_repr, async_tree_memoization, async_tree_memoization_tg, pprint_pformat, async_tree_cpu_io_mixed_tg, meteor_contest

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 99.57% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x