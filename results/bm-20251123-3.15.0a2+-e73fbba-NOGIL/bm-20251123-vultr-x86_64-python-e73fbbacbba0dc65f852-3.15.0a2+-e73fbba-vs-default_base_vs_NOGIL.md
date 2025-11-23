# Results vs. default_base_vs_NOGIL

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 281 ms: 1.13x slower                                                   |
| docutils       | 2.53 sec                                                               | 2.69 sec: 1.06x slower                                                 |
| html5lib       | 60.6 ms                                                                | 64.4 ms: 1.06x slower                                                  |
| sphinx         | 964 ms                                                                 | 1.06 sec: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 592 ms                                                                 | 519 ms: 1.14x faster                                                   |
| async_tree_none_tg        | 245 ms                                                                 | 228 ms: 1.07x faster                                                   |
| async_tree_memoization_tg | 307 ms                                                                 | 286 ms: 1.07x faster                                                   |
| asyncio_websockets        | 545 ms                                                                 | 509 ms: 1.07x faster                                                   |
| async_tree_io             | 559 ms                                                                 | 544 ms: 1.03x faster                                                   |
| async_tree_memoization    | 307 ms                                                                 | 311 ms: 1.01x slower                                                   |
| coroutines                | 24.0 ms                                                                | 25.1 ms: 1.04x slower                                                  |
| async_tree_none           | 246 ms                                                                 | 258 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed   | 486 ms                                                                 | 512 ms: 1.05x slower                                                   |
| async_generators          | 347 ms                                                                 | 376 ms: 1.08x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 192 ms: 1.01x faster                                                   |
| nbody          | 88.6 ms                                                                | 124 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 21.5 ms                                                                | 20.3 ms: 1.06x faster                                                  |
| regex_dna      | 173 ms                                                                 | 164 ms: 1.06x faster                                                   |
| regex_effbot   | 2.77 ms                                                                | 2.66 ms: 1.04x faster                                                  |
| regex_compile  | 125 ms                                                                 | 143 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                 | 132 ms: 1.01x slower                                                   |
| xml_etree_iterparse  | 85.2 ms                                                                | 88.7 ms: 1.04x slower                                                  |
| tomli_loads          | 1.91 sec                                                               | 2.04 sec: 1.06x slower                                                 |
| pickle_pure_python   | 307 us                                                                 | 337 us: 1.10x slower                                                   |
| unpickle_pure_python | 211 us                                                                 | 233 us: 1.10x slower                                                   |
| json_loads           | 28.5 us                                                                | 31.8 us: 1.11x slower                                                  |
| xml_etree_generate   | 82.9 ms                                                                | 95.7 ms: 1.15x slower                                                  |
| json_dumps           | 9.32 ms                                                                | 10.9 ms: 1.17x slower                                                  |
| xml_etree_process    | 58.1 ms                                                                | 69.0 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                | 15.7 ms: 1.27x slower                                                  |
| python_startup_no_site | 7.23 ms                                                                | 9.57 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 40.2 ms: 1.15x slower                                                  |
| genshi_xml      | 48.8 ms                                                                | 58.1 ms: 1.19x slower                                                  |
| genshi_text     | 20.6 ms                                                                | 26.7 ms: 1.30x slower                                                  |
| mako            | 11.6 ms                                                                | 15.8 ms: 1.36x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                           |

All benchmarks:
===============

| Benchmark                 | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal              | 4.08 ms                                                                | 1.93 ms: 2.12x faster                                                  |
| create_gc_cycles          | 1.92 ms                                                                | 1.50 ms: 1.28x faster                                                  |
| async_tree_io_tg          | 592 ms                                                                 | 519 ms: 1.14x faster                                                   |
| sqlite_synth              | 2.27 us                                                                | 2.03 us: 1.12x faster                                                  |
| async_tree_none_tg        | 245 ms                                                                 | 228 ms: 1.07x faster                                                   |
| async_tree_memoization_tg | 307 ms                                                                 | 286 ms: 1.07x faster                                                   |
| asyncio_websockets        | 545 ms                                                                 | 509 ms: 1.07x faster                                                   |
| regex_v8                  | 21.5 ms                                                                | 20.3 ms: 1.06x faster                                                  |
| regex_dna                 | 173 ms                                                                 | 164 ms: 1.06x faster                                                   |
| regex_effbot              | 2.77 ms                                                                | 2.66 ms: 1.04x faster                                                  |
| async_tree_io             | 559 ms                                                                 | 544 ms: 1.03x faster                                                   |
| pidigits                  | 193 ms                                                                 | 192 ms: 1.01x faster                                                   |
| pathlib                   | 17.5 ms                                                                | 17.7 ms: 1.01x slower                                                  |
| async_tree_memoization    | 307 ms                                                                 | 311 ms: 1.01x slower                                                   |
| xml_etree_parse           | 130 ms                                                                 | 132 ms: 1.01x slower                                                   |
| xml_etree_iterparse       | 85.2 ms                                                                | 88.7 ms: 1.04x slower                                                  |
| coroutines                | 24.0 ms                                                                | 25.1 ms: 1.04x slower                                                  |
| bpe_tokeniser             | 4.22 sec                                                               | 4.41 sec: 1.04x slower                                                 |
| json                      | 5.15 ms                                                                | 5.39 ms: 1.05x slower                                                  |
| async_tree_none           | 246 ms                                                                 | 258 ms: 1.05x slower                                                   |
| generators                | 28.9 ms                                                                | 30.4 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed   | 486 ms                                                                 | 512 ms: 1.05x slower                                                   |
| dulwich_log               | 68.0 ms                                                                | 71.9 ms: 1.06x slower                                                  |
| pylint                    | 288 ms                                                                 | 305 ms: 1.06x slower                                                   |
| docutils                  | 2.53 sec                                                               | 2.69 sec: 1.06x slower                                                 |
| html5lib                  | 60.6 ms                                                                | 64.4 ms: 1.06x slower                                                  |
| tomli_loads               | 1.91 sec                                                               | 2.04 sec: 1.06x slower                                                 |
| deltablue                 | 3.38 ms                                                                | 3.63 ms: 1.07x slower                                                  |
| async_generators          | 347 ms                                                                 | 376 ms: 1.08x slower                                                   |
| logging_silent            | 99.1 ns                                                                | 108 ns: 1.09x slower                                                   |
| pycparser                 | 1.07 sec                                                               | 1.17 sec: 1.09x slower                                                 |
| sympy_expand              | 473 ms                                                                 | 518 ms: 1.09x slower                                                   |
| pickle_pure_python        | 307 us                                                                 | 337 us: 1.10x slower                                                   |
| sphinx                    | 964 ms                                                                 | 1.06 sec: 1.10x slower                                                 |
| many_optionals            | 1.21 ms                                                                | 1.33 ms: 1.10x slower                                                  |
| unpickle_pure_python      | 211 us                                                                 | 233 us: 1.10x slower                                                   |
| telco                     | 156 ms                                                                 | 173 ms: 1.11x slower                                                   |
| chaos                     | 56.5 ms                                                                | 62.9 ms: 1.11x slower                                                  |
| json_loads                | 28.5 us                                                                | 31.8 us: 1.11x slower                                                  |
| scimark_sor               | 110 ms                                                                 | 123 ms: 1.12x slower                                                   |
| scimark_fft               | 308 ms                                                                 | 345 ms: 1.12x slower                                                   |
| sympy_str                 | 275 ms                                                                 | 309 ms: 1.12x slower                                                   |
| nqueens                   | 78.9 ms                                                                | 88.8 ms: 1.13x slower                                                  |
| hexiom                    | 5.71 ms                                                                | 6.44 ms: 1.13x slower                                                  |
| pprint_safe_repr          | 690 ms                                                                 | 779 ms: 1.13x slower                                                   |
| sqlglot_v2_normalize      | 103 ms                                                                 | 116 ms: 1.13x slower                                                   |
| thrift                    | 754 us                                                                 | 852 us: 1.13x slower                                                   |
| 2to3                      | 248 ms                                                                 | 281 ms: 1.13x slower                                                   |
| pprint_pformat            | 1.42 sec                                                               | 1.61 sec: 1.13x slower                                                 |
| go                        | 106 ms                                                                 | 121 ms: 1.14x slower                                                   |
| mdp                       | 1.15 sec                                                               | 1.31 sec: 1.14x slower                                                 |
| sympy_sum                 | 154 ms                                                                 | 176 ms: 1.14x slower                                                   |
| subparsers                | 44.7 ms                                                                | 51.1 ms: 1.14x slower                                                  |
| pyflate                   | 408 ms                                                                 | 467 ms: 1.15x slower                                                   |
| django_template           | 35.1 ms                                                                | 40.2 ms: 1.15x slower                                                  |
| regex_compile             | 125 ms                                                                 | 143 ms: 1.15x slower                                                   |
| sqlglot_v2_optimize       | 50.9 ms                                                                | 58.5 ms: 1.15x slower                                                  |
| comprehensions            | 15.6 us                                                                | 17.9 us: 1.15x slower                                                  |
| deepcopy_reduce           | 2.60 us                                                                | 3.00 us: 1.15x slower                                                  |
| sympy_integrate           | 18.9 ms                                                                | 21.8 ms: 1.15x slower                                                  |
| deepcopy                  | 242 us                                                                 | 279 us: 1.15x slower                                                   |
| xml_etree_generate        | 82.9 ms                                                                | 95.7 ms: 1.15x slower                                                  |
| deepcopy_memo             | 26.6 us                                                                | 30.9 us: 1.16x slower                                                  |
| json_dumps                | 9.32 ms                                                                | 10.9 ms: 1.17x slower                                                  |
| scimark_lu                | 112 ms                                                                 | 131 ms: 1.17x slower                                                   |
| fannkuch                  | 390 ms                                                                 | 458 ms: 1.18x slower                                                   |
| logging_simple            | 5.79 us                                                                | 6.83 us: 1.18x slower                                                  |
| raytrace                  | 249 ms                                                                 | 296 ms: 1.19x slower                                                   |
| xml_etree_process         | 58.1 ms                                                                | 69.0 ms: 1.19x slower                                                  |
| genshi_xml                | 48.8 ms                                                                | 58.1 ms: 1.19x slower                                                  |
| logging_format            | 6.55 us                                                                | 7.83 us: 1.19x slower                                                  |
| bench_mp_pool             | 12.9 ms                                                                | 15.6 ms: 1.21x slower                                                  |
| sqlglot_v2_transpile      | 1.50 ms                                                                | 1.82 ms: 1.21x slower                                                  |
| sqlglot_v2_parse          | 1.20 ms                                                                | 1.46 ms: 1.22x slower                                                  |
| spectral_norm             | 91.7 ms                                                                | 112 ms: 1.22x slower                                                   |
| typing_runtime_protocols  | 152 us                                                                 | 186 us: 1.22x slower                                                   |
| richards                  | 42.2 ms                                                                | 51.7 ms: 1.23x slower                                                  |
| meteor_contest            | 98.7 ms                                                                | 121 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult   | 4.44 ms                                                                | 5.50 ms: 1.24x slower                                                  |
| crypto_pyaes              | 69.7 ms                                                                | 86.3 ms: 1.24x slower                                                  |
| richards_super            | 48.0 ms                                                                | 59.8 ms: 1.25x slower                                                  |
| scimark_monte_carlo       | 62.3 ms                                                                | 78.6 ms: 1.26x slower                                                  |
| python_startup            | 12.3 ms                                                                | 15.7 ms: 1.27x slower                                                  |
| genshi_text               | 20.6 ms                                                                | 26.7 ms: 1.30x slower                                                  |
| python_startup_no_site    | 7.23 ms                                                                | 9.57 ms: 1.32x slower                                                  |
| coverage                  | 80.9 ms                                                                | 110 ms: 1.36x slower                                                   |
| mako                      | 11.6 ms                                                                | 15.8 ms: 1.36x slower                                                  |
| nbody                     | 88.6 ms                                                                | 124 ms: 1.40x slower                                                   |
| bench_thread_pool         | 1.08 ms                                                                | 3.17 ms: 2.93x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, float
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3/bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.20x