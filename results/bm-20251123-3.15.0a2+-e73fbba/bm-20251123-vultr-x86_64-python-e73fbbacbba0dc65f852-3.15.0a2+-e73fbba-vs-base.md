# Results vs. base

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.004x slower
- HPT reliability: 76.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                 |
| html5lib       | 60.6 ms                                                                | 61.5 ms: 1.01x slower                                                  |
| sphinx         | 964 ms                                                                 | 975 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators           | 347 ms                                                                 | 338 ms: 1.03x faster                                                   |
| async_tree_memoization_tg  | 307 ms                                                                 | 305 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                 | 527 ms: 1.08x slower                                                   |
| async_tree_cpu_io_mixed    | 486 ms                                                                 | 531 ms: 1.09x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (7): async_tree_io, coroutines, asyncio_websockets, async_tree_none_tg, async_tree_none, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 88.6 ms                                                                | 88.1 ms: 1.01x faster                                                  |
| pidigits       | 193 ms                                                                 | 220 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 125 ms                                                                 | 124 ms: 1.01x faster                                                   |
| regex_effbot   | 2.77 ms                                                                | 2.88 ms: 1.04x slower                                                  |
| regex_v8       | 21.5 ms                                                                | 22.7 ms: 1.06x slower                                                  |
| regex_dna      | 173 ms                                                                 | 188 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 211 us                                                                 | 210 us: 1.01x faster                                                   |
| tomli_loads          | 1.91 sec                                                               | 1.90 sec: 1.01x faster                                                 |
| json_loads           | 28.5 us                                                                | 28.4 us: 1.00x faster                                                  |
| pickle_pure_python   | 307 us                                                                 | 305 us: 1.00x faster                                                   |
| json_dumps           | 9.32 ms                                                                | 9.28 ms: 1.00x faster                                                  |
| xml_etree_iterparse  | 85.2 ms                                                                | 85.5 ms: 1.00x slower                                                  |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.23 ms                                                                | 7.26 ms: 1.00x slower                                                  |
| python_startup         | 12.3 ms                                                                | 12.4 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 34.3 ms: 1.02x faster                                                  |
| mako            | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                                | 48.5 ms: 1.01x faster                                                  |
| genshi_text     | 20.6 ms                                                                | 20.7 ms: 1.00x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 4.44 ms                                                                | 4.27 ms: 1.04x faster                                                  |
| generators                 | 28.9 ms                                                                | 28.0 ms: 1.03x faster                                                  |
| scimark_sor                | 110 ms                                                                 | 107 ms: 1.03x faster                                                   |
| async_generators           | 347 ms                                                                 | 338 ms: 1.03x faster                                                   |
| sqlglot_v2_normalize       | 103 ms                                                                 | 100 ms: 1.03x faster                                                   |
| django_template            | 35.1 ms                                                                | 34.3 ms: 1.02x faster                                                  |
| go                         | 106 ms                                                                 | 104 ms: 1.02x faster                                                   |
| deltablue                  | 3.38 ms                                                                | 3.32 ms: 1.02x faster                                                  |
| json                       | 5.15 ms                                                                | 5.07 ms: 1.02x faster                                                  |
| mako                       | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                                  |
| chaos                      | 56.5 ms                                                                | 55.8 ms: 1.01x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.01x faster                                                   |
| hexiom                     | 5.71 ms                                                                | 5.64 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.27 us                                                                | 2.24 us: 1.01x faster                                                  |
| raytrace                   | 249 ms                                                                 | 246 ms: 1.01x faster                                                   |
| logging_silent             | 99.1 ns                                                                | 97.9 ns: 1.01x faster                                                  |
| nqueens                    | 78.9 ms                                                                | 78.1 ms: 1.01x faster                                                  |
| pathlib                    | 17.5 ms                                                                | 17.3 ms: 1.01x faster                                                  |
| crypto_pyaes               | 69.7 ms                                                                | 69.0 ms: 1.01x faster                                                  |
| richards                   | 42.2 ms                                                                | 41.8 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 211 us                                                                 | 210 us: 1.01x faster                                                   |
| tomli_loads                | 1.91 sec                                                               | 1.90 sec: 1.01x faster                                                 |
| scimark_monte_carlo        | 62.3 ms                                                                | 61.8 ms: 1.01x faster                                                  |
| regex_compile              | 125 ms                                                                 | 124 ms: 1.01x faster                                                   |
| nbody                      | 88.6 ms                                                                | 88.1 ms: 1.01x faster                                                  |
| sqlglot_v2_optimize        | 50.9 ms                                                                | 50.6 ms: 1.01x faster                                                  |
| subparsers                 | 44.7 ms                                                                | 44.4 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                                | 48.5 ms: 1.01x faster                                                  |
| fannkuch                   | 390 ms                                                                 | 387 ms: 1.01x faster                                                   |
| async_tree_memoization_tg  | 307 ms                                                                 | 305 ms: 1.01x faster                                                   |
| richards_super             | 48.0 ms                                                                | 47.8 ms: 1.01x faster                                                  |
| json_loads                 | 28.5 us                                                                | 28.4 us: 1.00x faster                                                  |
| pickle_pure_python         | 307 us                                                                 | 305 us: 1.00x faster                                                   |
| json_dumps                 | 9.32 ms                                                                | 9.28 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.22 sec                                                               | 4.21 sec: 1.00x faster                                                 |
| mdp                        | 1.15 sec                                                               | 1.15 sec: 1.00x faster                                                 |
| sympy_integrate            | 18.9 ms                                                                | 19.0 ms: 1.00x slower                                                  |
| xml_etree_iterparse        | 85.2 ms                                                                | 85.5 ms: 1.00x slower                                                  |
| genshi_text                | 20.6 ms                                                                | 20.7 ms: 1.00x slower                                                  |
| python_startup_no_site     | 7.23 ms                                                                | 7.26 ms: 1.00x slower                                                  |
| pprint_pformat             | 1.42 sec                                                               | 1.43 sec: 1.01x slower                                                 |
| python_startup             | 12.3 ms                                                                | 12.4 ms: 1.01x slower                                                  |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                   |
| docutils                   | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                                   |
| deepcopy                   | 242 us                                                                 | 244 us: 1.01x slower                                                   |
| deepcopy_reduce            | 2.60 us                                                                | 2.63 us: 1.01x slower                                                  |
| sphinx                     | 964 ms                                                                 | 975 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 690 ms                                                                 | 698 ms: 1.01x slower                                                   |
| comprehensions             | 15.6 us                                                                | 15.8 us: 1.01x slower                                                  |
| telco                      | 156 ms                                                                 | 158 ms: 1.01x slower                                                   |
| html5lib                   | 60.6 ms                                                                | 61.5 ms: 1.01x slower                                                  |
| bench_mp_pool              | 12.9 ms                                                                | 13.1 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 152 us                                                                 | 155 us: 1.02x slower                                                   |
| spectral_norm              | 91.7 ms                                                                | 93.9 ms: 1.02x slower                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.88 ms: 1.04x slower                                                  |
| regex_v8                   | 21.5 ms                                                                | 22.7 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                 | 527 ms: 1.08x slower                                                   |
| regex_dna                  | 173 ms                                                                 | 188 ms: 1.08x slower                                                   |
| async_tree_cpu_io_mixed    | 486 ms                                                                 | 531 ms: 1.09x slower                                                   |
| pidigits                   | 193 ms                                                                 | 220 ms: 1.14x slower                                                   |
| gc_traversal               | 4.08 ms                                                                | 4.78 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (29): sympy_expand, async_tree_io, coroutines, pycparser, many_optionals, scimark_fft, 2to3, sympy_str, asyncio_websockets, pyflate, sqlglot_v2_transpile, xml_etree_generate, bench_thread_pool, xml_etree_process, dulwich_log, deepcopy_memo, coverage, async_tree_none_tg, async_tree_none, sqlglot_v2_parse, async_tree_io_tg, pylint, meteor_contest, async_tree_memoization, logging_simple, float, create_gc_cycles, thrift, logging_format
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3/bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 76.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x