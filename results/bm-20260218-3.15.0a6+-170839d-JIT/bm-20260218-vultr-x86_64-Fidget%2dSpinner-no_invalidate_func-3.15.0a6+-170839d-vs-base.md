# Results vs. base

- fork: Fidget-Spinner
- ref: no_invalidate_func
- machine: linux-x86_64
- commit hash: 170839d
- commit date: 2026-02-18
- overall geometric mean: 1.006x faster
- HPT reliability: 78.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| html5lib       | 62.3 ms                                                                | 63.6 ms: 1.02x slower                                                          |
| sphinx         | 1.01 sec                                                               | 1.00 sec: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 479 ms                                                                 | 472 ms: 1.02x faster                                                           |
| async_generators        | 358 ms                                                                 | 366 ms: 1.02x slower                                                           |
| coroutines              | 23.8 ms                                                                | 24.4 ms: 1.02x slower                                                          |
| async_tree_io           | 573 ms                                                                 | 591 ms: 1.03x slower                                                           |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_io_tg, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 73.3 ms                                                                | 74.2 ms: 1.01x slower                                                          |
| pidigits       | 199 ms                                                                 | 202 ms: 1.02x slower                                                           |
| float          | 59.8 ms                                                                | 60.8 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8       | 23.0 ms                                                                | 22.0 ms: 1.04x faster                                                          |
| regex_compile  | 124 ms                                                                 | 125 ms: 1.01x slower                                                           |
| regex_dna      | 178 ms                                                                 | 185 ms: 1.04x slower                                                           |
| regex_effbot   | 2.73 ms                                                                | 2.89 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 1.64 sec                                                               | 1.57 sec: 1.05x faster                                                         |
| json_dumps           | 9.08 ms                                                                | 8.96 ms: 1.01x faster                                                          |
| xml_etree_process    | 54.6 ms                                                                | 54.1 ms: 1.01x faster                                                          |
| xml_etree_iterparse  | 83.8 ms                                                                | 84.1 ms: 1.00x slower                                                          |
| unpickle_pure_python | 198 us                                                                 | 200 us: 1.01x slower                                                           |
| json_loads           | 28.5 us                                                                | 28.8 us: 1.01x slower                                                          |
| pickle_pure_python   | 306 us                                                                 | 311 us: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.43 ms                                                                | 7.40 ms: 1.00x faster                                                          |
| python_startup         | 12.7 ms                                                                | 12.6 ms: 1.00x faster                                                          |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 35.3 ms                                                                | 36.0 ms: 1.02x slower                                                          |
| mako            | 10.3 ms                                                                | 10.5 ms: 1.02x slower                                                          |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                                   |

All benchmarks:
===============

| Benchmark               | bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| gc_traversal            | 4.66 ms                                                                | 4.16 ms: 1.12x faster                                                          |
| mdp                     | 1.34 sec                                                               | 1.21 sec: 1.11x faster                                                         |
| sympy_str               | 314 ms                                                                 | 286 ms: 1.10x faster                                                           |
| comprehensions          | 15.9 us                                                                | 14.6 us: 1.09x faster                                                          |
| sympy_sum               | 175 ms                                                                 | 161 ms: 1.09x faster                                                           |
| hexiom                  | 6.20 ms                                                                | 5.76 ms: 1.08x faster                                                          |
| sympy_expand            | 524 ms                                                                 | 491 ms: 1.07x faster                                                           |
| pylint                  | 310 ms                                                                 | 292 ms: 1.06x faster                                                           |
| sympy_integrate         | 20.7 ms                                                                | 19.6 ms: 1.06x faster                                                          |
| sqlglot_v2_normalize    | 110 ms                                                                 | 104 ms: 1.05x faster                                                           |
| tomli_loads             | 1.64 sec                                                               | 1.57 sec: 1.05x faster                                                         |
| create_gc_cycles        | 1.91 ms                                                                | 1.83 ms: 1.04x faster                                                          |
| regex_v8                | 23.0 ms                                                                | 22.0 ms: 1.04x faster                                                          |
| generators              | 30.3 ms                                                                | 29.1 ms: 1.04x faster                                                          |
| sqlglot_v2_optimize     | 54.0 ms                                                                | 51.9 ms: 1.04x faster                                                          |
| subparsers              | 9.19 ms                                                                | 8.85 ms: 1.04x faster                                                          |
| nqueens                 | 81.6 ms                                                                | 78.6 ms: 1.04x faster                                                          |
| go                      | 101 ms                                                                 | 99.3 ms: 1.02x faster                                                          |
| pathlib                 | 17.7 ms                                                                | 17.4 ms: 1.02x faster                                                          |
| logging_simple          | 6.01 us                                                                | 5.89 us: 1.02x faster                                                          |
| many_optionals          | 992 us                                                                 | 976 us: 1.02x faster                                                           |
| async_tree_cpu_io_mixed | 479 ms                                                                 | 472 ms: 1.02x faster                                                           |
| json_dumps              | 9.08 ms                                                                | 8.96 ms: 1.01x faster                                                          |
| sqlglot_v2_transpile    | 1.49 ms                                                                | 1.48 ms: 1.01x faster                                                          |
| xml_etree_process       | 54.6 ms                                                                | 54.1 ms: 1.01x faster                                                          |
| sphinx                  | 1.01 sec                                                               | 1.00 sec: 1.01x faster                                                         |
| logging_silent          | 85.3 ns                                                                | 84.8 ns: 1.01x faster                                                          |
| python_startup_no_site  | 7.43 ms                                                                | 7.40 ms: 1.00x faster                                                          |
| shortest_path           | 423 ms                                                                 | 421 ms: 1.00x faster                                                           |
| python_startup          | 12.7 ms                                                                | 12.6 ms: 1.00x faster                                                          |
| xml_etree_iterparse     | 83.8 ms                                                                | 84.1 ms: 1.00x slower                                                          |
| k_core                  | 1.83 sec                                                               | 1.84 sec: 1.01x slower                                                         |
| deltablue               | 2.79 ms                                                                | 2.81 ms: 1.01x slower                                                          |
| sqlglot_v2_parse        | 1.18 ms                                                                | 1.18 ms: 1.01x slower                                                          |
| pyflate                 | 367 ms                                                                 | 370 ms: 1.01x slower                                                           |
| fannkuch                | 349 ms                                                                 | 352 ms: 1.01x slower                                                           |
| unpickle_pure_python    | 198 us                                                                 | 200 us: 1.01x slower                                                           |
| regex_compile           | 124 ms                                                                 | 125 ms: 1.01x slower                                                           |
| meteor_contest          | 98.3 ms                                                                | 99.4 ms: 1.01x slower                                                          |
| crypto_pyaes            | 65.3 ms                                                                | 66.0 ms: 1.01x slower                                                          |
| json                    | 4.97 ms                                                                | 5.02 ms: 1.01x slower                                                          |
| nbody                   | 73.3 ms                                                                | 74.2 ms: 1.01x slower                                                          |
| connected_components    | 374 ms                                                                 | 378 ms: 1.01x slower                                                           |
| json_loads              | 28.5 us                                                                | 28.8 us: 1.01x slower                                                          |
| raytrace                | 284 ms                                                                 | 288 ms: 1.01x slower                                                           |
| coverage                | 81.1 ms                                                                | 82.3 ms: 1.01x slower                                                          |
| scimark_lu              | 79.4 ms                                                                | 80.6 ms: 1.01x slower                                                          |
| pidigits                | 199 ms                                                                 | 202 ms: 1.02x slower                                                           |
| deepcopy_memo           | 22.6 us                                                                | 23.0 us: 1.02x slower                                                          |
| float                   | 59.8 ms                                                                | 60.8 ms: 1.02x slower                                                          |
| sqlite_synth            | 2.12 us                                                                | 2.16 us: 1.02x slower                                                          |
| scimark_fft             | 255 ms                                                                 | 259 ms: 1.02x slower                                                           |
| pickle_pure_python      | 306 us                                                                 | 311 us: 1.02x slower                                                           |
| richards_super          | 22.0 ms                                                                | 22.4 ms: 1.02x slower                                                          |
| django_template         | 35.3 ms                                                                | 36.0 ms: 1.02x slower                                                          |
| mako                    | 10.3 ms                                                                | 10.5 ms: 1.02x slower                                                          |
| scimark_monte_carlo     | 51.7 ms                                                                | 52.7 ms: 1.02x slower                                                          |
| chaos                   | 53.7 ms                                                                | 54.7 ms: 1.02x slower                                                          |
| deepcopy                | 224 us                                                                 | 228 us: 1.02x slower                                                           |
| richards                | 18.1 ms                                                                | 18.4 ms: 1.02x slower                                                          |
| html5lib                | 62.3 ms                                                                | 63.6 ms: 1.02x slower                                                          |
| async_generators        | 358 ms                                                                 | 366 ms: 1.02x slower                                                           |
| coroutines              | 23.8 ms                                                                | 24.4 ms: 1.02x slower                                                          |
| pprint_pformat          | 1.28 sec                                                               | 1.31 sec: 1.03x slower                                                         |
| async_tree_io           | 573 ms                                                                 | 591 ms: 1.03x slower                                                           |
| dulwich_log             | 69.7 ms                                                                | 72.1 ms: 1.03x slower                                                          |
| regex_dna               | 178 ms                                                                 | 185 ms: 1.04x slower                                                           |
| scimark_sparse_mat_mult | 4.06 ms                                                                | 4.26 ms: 1.05x slower                                                          |
| regex_effbot            | 2.73 ms                                                                | 2.89 ms: 1.06x slower                                                          |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (23): async_tree_memoization, async_tree_cpu_io_mixed_tg, logging_format, xml_etree_generate, scimark_sor, 2to3, async_tree_memoization_tg, xml_etree_parse, spectral_norm, bench_thread_pool, asyncio_websockets, async_tree_io_tg, docutils, pprint_safe_repr, bpe_tokeniser, thrift, pycparser, async_tree_none_tg, async_tree_none, telco, deepcopy_reduce, typing_runtime_protocols, bench_mp_pool
Ignored benchmarks (8) of results/bm-20260214-3.15.0a6+-645f5c4-JIT/bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 78.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x