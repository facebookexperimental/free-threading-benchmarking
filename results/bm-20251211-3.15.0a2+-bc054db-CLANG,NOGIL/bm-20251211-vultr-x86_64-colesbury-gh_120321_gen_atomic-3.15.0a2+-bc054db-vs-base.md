# Results vs. base

- fork: colesbury
- ref: gh_120321_gen_atomic
- machine: linux-x86_64
- commit hash: bc054db
- commit date: 2025-12-11
- overall geometric mean: 1.003x slower
- HPT reliability: 91.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 269 ms: 1.01x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 61.6 ms                                                                | 63.1 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines     | 23.1 ms                                                                | 22.5 ms: 1.02x faster                                                     |
| async_tree_io  | 592 ms                                                                 | 604 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (9): async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 187 ms: 1.10x faster                                                      |
| nbody          | 117 ms                                                                 | 115 ms: 1.01x faster                                                      |
| float          | 69.5 ms                                                                | 68.8 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.03 ms                                                                | 2.91 ms: 1.04x faster                                                     |
| regex_compile  | 134 ms                                                                 | 134 ms: 1.00x slower                                                      |
| regex_dna      | 180 ms                                                                 | 182 ms: 1.01x slower                                                      |
| regex_v8       | 21.4 ms                                                                | 21.8 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_loads           | 26.9 us                                                                | 27.1 us: 1.01x slower                                                     |
| unpickle_pure_python | 223 us                                                                 | 225 us: 1.01x slower                                                      |
| xml_etree_process    | 61.9 ms                                                                | 62.4 ms: 1.01x slower                                                     |
| tomli_loads          | 2.19 sec                                                               | 2.21 sec: 1.01x slower                                                    |
| pickle_pure_python   | 312 us                                                                 | 317 us: 1.01x slower                                                      |
| xml_etree_parse      | 146 ms                                                                 | 148 ms: 1.02x slower                                                      |
| xml_etree_iterparse  | 91.5 ms                                                                | 93.4 ms: 1.02x slower                                                     |
| json_dumps           | 9.51 ms                                                                | 9.75 ms: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                                | 9.62 ms: 1.00x slower                                                     |
| python_startup         | 15.6 ms                                                                | 15.6 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                                | 23.9 ms: 1.01x slower                                                     |
| mako           | 14.7 ms                                                                | 14.9 ms: 1.01x slower                                                     |
| genshi_xml     | 52.2 ms                                                                | 52.9 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits                 | 206 ms                                                                 | 187 ms: 1.10x faster                                                      |
| regex_effbot             | 3.03 ms                                                                | 2.91 ms: 1.04x faster                                                     |
| coroutines               | 23.1 ms                                                                | 22.5 ms: 1.02x faster                                                     |
| logging_format           | 7.35 us                                                                | 7.19 us: 1.02x faster                                                     |
| scimark_sor              | 112 ms                                                                 | 110 ms: 1.02x faster                                                      |
| logging_simple           | 6.36 us                                                                | 6.24 us: 1.02x faster                                                     |
| logging_silent           | 90.8 ns                                                                | 89.5 ns: 1.02x faster                                                     |
| nbody                    | 117 ms                                                                 | 115 ms: 1.01x faster                                                      |
| sympy_expand             | 502 ms                                                                 | 496 ms: 1.01x faster                                                      |
| shortest_path            | 520 ms                                                                 | 513 ms: 1.01x faster                                                      |
| float                    | 69.5 ms                                                                | 68.8 ms: 1.01x faster                                                     |
| deepcopy_memo            | 29.1 us                                                                | 28.8 us: 1.01x faster                                                     |
| sympy_integrate          | 20.6 ms                                                                | 20.4 ms: 1.01x faster                                                     |
| scimark_lu               | 113 ms                                                                 | 112 ms: 1.01x faster                                                      |
| sympy_sum                | 167 ms                                                                 | 166 ms: 1.01x faster                                                      |
| telco                    | 166 ms                                                                 | 165 ms: 1.01x faster                                                      |
| raytrace                 | 275 ms                                                                 | 274 ms: 1.01x faster                                                      |
| sympy_str                | 296 ms                                                                 | 295 ms: 1.01x faster                                                      |
| scimark_monte_carlo      | 68.9 ms                                                                | 68.5 ms: 1.01x faster                                                     |
| deepcopy                 | 247 us                                                                 | 246 us: 1.00x faster                                                      |
| regex_compile            | 134 ms                                                                 | 134 ms: 1.00x slower                                                      |
| python_startup_no_site   | 9.59 ms                                                                | 9.62 ms: 1.00x slower                                                     |
| connected_components     | 478 ms                                                                 | 480 ms: 1.00x slower                                                      |
| pprint_safe_repr         | 726 ms                                                                 | 730 ms: 1.00x slower                                                      |
| fannkuch                 | 404 ms                                                                 | 406 ms: 1.00x slower                                                      |
| crypto_pyaes             | 80.7 ms                                                                | 81.2 ms: 1.01x slower                                                     |
| 2to3                     | 267 ms                                                                 | 269 ms: 1.01x slower                                                      |
| python_startup           | 15.6 ms                                                                | 15.6 ms: 1.01x slower                                                     |
| meteor_contest           | 117 ms                                                                 | 118 ms: 1.01x slower                                                      |
| pprint_pformat           | 1.50 sec                                                               | 1.51 sec: 1.01x slower                                                    |
| json_loads               | 26.9 us                                                                | 27.1 us: 1.01x slower                                                     |
| unpickle_pure_python     | 223 us                                                                 | 225 us: 1.01x slower                                                      |
| docutils                 | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| hexiom                   | 6.26 ms                                                                | 6.30 ms: 1.01x slower                                                     |
| richards                 | 44.6 ms                                                                | 45.0 ms: 1.01x slower                                                     |
| gc_traversal             | 2.24 ms                                                                | 2.26 ms: 1.01x slower                                                     |
| bench_mp_pool            | 7.27 ms                                                                | 7.32 ms: 1.01x slower                                                     |
| xml_etree_process        | 61.9 ms                                                                | 62.4 ms: 1.01x slower                                                     |
| scimark_fft              | 309 ms                                                                 | 311 ms: 1.01x slower                                                      |
| sqlite_synth             | 2.01 us                                                                | 2.03 us: 1.01x slower                                                     |
| bpe_tokeniser            | 4.22 sec                                                               | 4.26 sec: 1.01x slower                                                    |
| genshi_text              | 23.7 ms                                                                | 23.9 ms: 1.01x slower                                                     |
| mako                     | 14.7 ms                                                                | 14.9 ms: 1.01x slower                                                     |
| regex_dna                | 180 ms                                                                 | 182 ms: 1.01x slower                                                      |
| tomli_loads              | 2.19 sec                                                               | 2.21 sec: 1.01x slower                                                    |
| typing_runtime_protocols | 167 us                                                                 | 169 us: 1.01x slower                                                      |
| genshi_xml               | 52.2 ms                                                                | 52.9 ms: 1.01x slower                                                     |
| pyflate                  | 429 ms                                                                 | 435 ms: 1.01x slower                                                      |
| pickle_pure_python       | 312 us                                                                 | 317 us: 1.01x slower                                                      |
| mdp                      | 1.26 sec                                                               | 1.28 sec: 1.02x slower                                                    |
| regex_v8                 | 21.4 ms                                                                | 21.8 ms: 1.02x slower                                                     |
| xml_etree_parse          | 146 ms                                                                 | 148 ms: 1.02x slower                                                      |
| dulwich_log              | 71.2 ms                                                                | 72.4 ms: 1.02x slower                                                     |
| nqueens                  | 81.9 ms                                                                | 83.5 ms: 1.02x slower                                                     |
| create_gc_cycles         | 1.50 ms                                                                | 1.53 ms: 1.02x slower                                                     |
| xml_etree_iterparse      | 91.5 ms                                                                | 93.4 ms: 1.02x slower                                                     |
| spectral_norm            | 99.1 ms                                                                | 101 ms: 1.02x slower                                                      |
| async_tree_io            | 592 ms                                                                 | 604 ms: 1.02x slower                                                      |
| html5lib                 | 61.6 ms                                                                | 63.1 ms: 1.02x slower                                                     |
| json_dumps               | 9.51 ms                                                                | 9.75 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult  | 4.86 ms                                                                | 5.02 ms: 1.03x slower                                                     |
| generators               | 28.5 ms                                                                | 31.4 ms: 1.10x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (32): sqlglot_v2_transpile, async_tree_io_tg, async_tree_none_tg, pylint, go, sqlglot_v2_parse, async_tree_memoization, thrift, async_tree_none, django_template, async_tree_cpu_io_mixed, pycparser, async_tree_memoization_tg, chaos, sphinx, async_tree_cpu_io_mixed_tg, subparsers, async_generators, asyncio_websockets, deltablue, k_core, comprehensions, sqlglot_v2_normalize, bench_thread_pool, xml_etree_generate, json, pathlib, deepcopy_reduce, sqlglot_v2_optimize, richards_super, coverage, many_optionals

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 91.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x