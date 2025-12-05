# Results vs. base

- fork: maurycy
- ref: maurycy_tuple_early
- machine: linux-x86_64
- commit hash: 0eae50d
- commit date: 2025-12-02
- overall geometric mean: 1.002x faster
- HPT reliability: 61.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 247 ms: 1.00x faster                                                   |
| docutils       | 2.58 sec                                                               | 2.55 sec: 1.01x faster                                                 |
| html5lib       | 61.3 ms                                                                | 61.7 ms: 1.01x slower                                                  |
| sphinx         | 966 ms                                                                 | 979 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|--------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 545 ms                                                                 | 544 ms: 1.00x faster                                                   |
| async_generators   | 338 ms                                                                 | 341 ms: 1.01x slower                                                   |
| async_tree_io_tg   | 583 ms                                                                 | 589 ms: 1.01x slower                                                   |
| async_tree_none_tg | 242 ms                                                                 | 246 ms: 1.02x slower                                                   |
| coroutines         | 23.6 ms                                                                | 24.4 ms: 1.04x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 69.9 ms                                                                | 68.6 ms: 1.02x faster                                                  |
| nbody          | 88.2 ms                                                                | 89.4 ms: 1.01x slower                                                  |
| pidigits       | 199 ms                                                                 | 203 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 171 ms: 1.05x faster                                                   |
| regex_effbot   | 2.77 ms                                                                | 2.64 ms: 1.05x faster                                                  |
| regex_v8       | 23.3 ms                                                                | 22.2 ms: 1.05x faster                                                  |
| regex_compile  | 124 ms                                                                 | 124 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 28.3 us                                                                | 27.6 us: 1.02x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 209 us: 1.02x faster                                                   |
| pickle_pure_python   | 308 us                                                                 | 305 us: 1.01x faster                                                   |
| xml_etree_generate   | 82.4 ms                                                                | 82.1 ms: 1.00x faster                                                  |
| xml_etree_process    | 58.0 ms                                                                | 58.2 ms: 1.00x slower                                                  |
| json_dumps           | 9.60 ms                                                                | 9.66 ms: 1.01x slower                                                  |
| xml_etree_iterparse  | 84.1 ms                                                                | 84.9 ms: 1.01x slower                                                  |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                  |
| python_startup_no_site | 7.27 ms                                                                | 7.25 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.5 ms                                                                | 11.7 ms: 1.01x slower                                                  |
| genshi_text    | 20.4 ms                                                                | 20.7 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                | bm-20251027-vultr-x86_64-python-1753ccb43223b0a1054a-3.15.0a1+-1753ccb | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| spectral_norm            | 96.3 ms                                                                | 90.9 ms: 1.06x faster                                                  |
| regex_dna                | 180 ms                                                                 | 171 ms: 1.05x faster                                                   |
| regex_effbot             | 2.77 ms                                                                | 2.64 ms: 1.05x faster                                                  |
| regex_v8                 | 23.3 ms                                                                | 22.2 ms: 1.05x faster                                                  |
| deltablue                | 3.24 ms                                                                | 3.10 ms: 1.05x faster                                                  |
| deepcopy_reduce          | 2.67 us                                                                | 2.58 us: 1.03x faster                                                  |
| scimark_fft              | 312 ms                                                                 | 302 ms: 1.03x faster                                                   |
| deepcopy                 | 250 us                                                                 | 242 us: 1.03x faster                                                   |
| json_loads               | 28.3 us                                                                | 27.6 us: 1.02x faster                                                  |
| telco                    | 160 ms                                                                 | 156 ms: 1.02x faster                                                   |
| json                     | 5.03 ms                                                                | 4.93 ms: 1.02x faster                                                  |
| crypto_pyaes             | 69.6 ms                                                                | 68.2 ms: 1.02x faster                                                  |
| generators               | 28.7 ms                                                                | 28.1 ms: 1.02x faster                                                  |
| sqlglot_v2_parse         | 1.21 ms                                                                | 1.19 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult  | 4.41 ms                                                                | 4.32 ms: 1.02x faster                                                  |
| float                    | 69.9 ms                                                                | 68.6 ms: 1.02x faster                                                  |
| unpickle_pure_python     | 213 us                                                                 | 209 us: 1.02x faster                                                   |
| typing_runtime_protocols | 155 us                                                                 | 153 us: 1.01x faster                                                   |
| hexiom                   | 5.78 ms                                                                | 5.70 ms: 1.01x faster                                                  |
| bench_thread_pool        | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                  |
| nqueens                  | 78.9 ms                                                                | 78.1 ms: 1.01x faster                                                  |
| sqlglot_v2_transpile     | 1.50 ms                                                                | 1.48 ms: 1.01x faster                                                  |
| comprehensions           | 15.8 us                                                                | 15.7 us: 1.01x faster                                                  |
| coverage                 | 81.9 ms                                                                | 81.2 ms: 1.01x faster                                                  |
| docutils                 | 2.58 sec                                                               | 2.55 sec: 1.01x faster                                                 |
| scimark_sor              | 108 ms                                                                 | 107 ms: 1.01x faster                                                   |
| pickle_pure_python       | 308 us                                                                 | 305 us: 1.01x faster                                                   |
| scimark_monte_carlo      | 61.6 ms                                                                | 61.2 ms: 1.01x faster                                                  |
| sympy_sum                | 155 ms                                                                 | 154 ms: 1.01x faster                                                   |
| bpe_tokeniser            | 4.20 sec                                                               | 4.17 sec: 1.01x faster                                                 |
| python_startup           | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                  |
| fannkuch                 | 392 ms                                                                 | 390 ms: 1.00x faster                                                   |
| 2to3                     | 249 ms                                                                 | 247 ms: 1.00x faster                                                   |
| pyflate                  | 414 ms                                                                 | 412 ms: 1.00x faster                                                   |
| k_core                   | 1.89 sec                                                               | 1.88 sec: 1.00x faster                                                 |
| create_gc_cycles         | 1.86 ms                                                                | 1.86 ms: 1.00x faster                                                  |
| xml_etree_generate       | 82.4 ms                                                                | 82.1 ms: 1.00x faster                                                  |
| python_startup_no_site   | 7.27 ms                                                                | 7.25 ms: 1.00x faster                                                  |
| asyncio_websockets       | 545 ms                                                                 | 544 ms: 1.00x faster                                                   |
| mdp                      | 1.15 sec                                                               | 1.15 sec: 1.00x faster                                                 |
| shortest_path            | 431 ms                                                                 | 431 ms: 1.00x faster                                                   |
| sqlglot_v2_optimize      | 50.6 ms                                                                | 50.7 ms: 1.00x slower                                                  |
| pycparser                | 1.10 sec                                                               | 1.10 sec: 1.00x slower                                                 |
| xml_etree_process        | 58.0 ms                                                                | 58.2 ms: 1.00x slower                                                  |
| connected_components     | 393 ms                                                                 | 394 ms: 1.00x slower                                                   |
| go                       | 105 ms                                                                 | 105 ms: 1.00x slower                                                   |
| regex_compile            | 124 ms                                                                 | 124 ms: 1.01x slower                                                   |
| subparsers               | 44.6 ms                                                                | 44.9 ms: 1.01x slower                                                  |
| json_dumps               | 9.60 ms                                                                | 9.66 ms: 1.01x slower                                                  |
| sqlglot_v2_normalize     | 100 ms                                                                 | 101 ms: 1.01x slower                                                   |
| sympy_str                | 271 ms                                                                 | 273 ms: 1.01x slower                                                   |
| html5lib                 | 61.3 ms                                                                | 61.7 ms: 1.01x slower                                                  |
| xml_etree_iterparse      | 84.1 ms                                                                | 84.9 ms: 1.01x slower                                                  |
| async_generators         | 338 ms                                                                 | 341 ms: 1.01x slower                                                   |
| sqlite_synth             | 2.24 us                                                                | 2.26 us: 1.01x slower                                                  |
| pathlib                  | 17.6 ms                                                                | 17.7 ms: 1.01x slower                                                  |
| async_tree_io_tg         | 583 ms                                                                 | 589 ms: 1.01x slower                                                   |
| richards_super           | 46.9 ms                                                                | 47.4 ms: 1.01x slower                                                  |
| richards                 | 41.1 ms                                                                | 41.6 ms: 1.01x slower                                                  |
| pprint_pformat           | 1.41 sec                                                               | 1.43 sec: 1.01x slower                                                 |
| pprint_safe_repr         | 694 ms                                                                 | 703 ms: 1.01x slower                                                   |
| nbody                    | 88.2 ms                                                                | 89.4 ms: 1.01x slower                                                  |
| sympy_expand             | 461 ms                                                                 | 467 ms: 1.01x slower                                                   |
| sphinx                   | 966 ms                                                                 | 979 ms: 1.01x slower                                                   |
| xml_etree_parse          | 128 ms                                                                 | 130 ms: 1.01x slower                                                   |
| mako                     | 11.5 ms                                                                | 11.7 ms: 1.01x slower                                                  |
| genshi_text              | 20.4 ms                                                                | 20.7 ms: 1.02x slower                                                  |
| async_tree_none_tg       | 242 ms                                                                 | 246 ms: 1.02x slower                                                   |
| logging_silent           | 96.0 ns                                                                | 97.8 ns: 1.02x slower                                                  |
| pidigits                 | 199 ms                                                                 | 203 ms: 1.02x slower                                                   |
| many_optionals           | 1.21 ms                                                                | 1.24 ms: 1.02x slower                                                  |
| logging_simple           | 5.93 us                                                                | 6.09 us: 1.03x slower                                                  |
| logging_format           | 6.77 us                                                                | 7.00 us: 1.03x slower                                                  |
| coroutines               | 23.6 ms                                                                | 24.4 ms: 1.04x slower                                                  |
| gc_traversal             | 4.25 ms                                                                | 4.58 ms: 1.08x slower                                                  |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (19): bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, genshi_xml, tomli_loads, raytrace, sympy_integrate, meteor_contest, chaos, thrift, dulwich_log, deepcopy_memo, scimark_lu, django_template, async_tree_memoization_tg, pylint, async_tree_io, async_tree_memoization, async_tree_none

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 61.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x