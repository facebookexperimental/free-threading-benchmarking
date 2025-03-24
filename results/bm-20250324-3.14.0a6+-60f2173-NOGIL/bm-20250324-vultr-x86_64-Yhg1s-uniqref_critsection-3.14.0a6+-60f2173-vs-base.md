# Results vs. base

- fork: Yhg1s
- ref: uniqref_critsection
- machine: linux-x86_64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 297 ms: 1.01x faster                                                 |
| html5lib       | 71.5 ms                                                                | 70.4 ms: 1.02x faster                                                |
| sphinx         | 1.10 sec                                                               | 1.10 sec: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators           | 384 ms                                                                 | 375 ms: 1.02x faster                                                 |
| coroutines                 | 23.5 ms                                                                | 23.0 ms: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 518 ms: 1.00x slower                                                 |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| async_tree_memoization     | 331 ms                                                                 | 334 ms: 1.01x slower                                                 |
| async_tree_io              | 582 ms                                                                 | 588 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 537 ms: 1.11x slower                                                 |
| async_tree_cpu_io_mixed    | 515 ms                                                                 | 572 ms: 1.11x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 137 ms                                                                 | 131 ms: 1.05x faster                                                 |
| float          | 76.8 ms                                                                | 76.4 ms: 1.00x faster                                                |
| pidigits       | 193 ms                                                                 | 223 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                                |
| regex_compile  | 158 ms                                                                 | 152 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                                 | 174 ms: 1.03x faster                                                 |
| regex_effbot   | 2.64 ms                                                                | 2.77 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_generate   | 98.3 ms                                                                | 95.5 ms: 1.03x faster                                                |
| tomli_loads          | 2.35 sec                                                               | 2.29 sec: 1.03x faster                                               |
| xml_etree_process    | 71.2 ms                                                                | 69.6 ms: 1.02x faster                                                |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                 |
| unpickle_pure_python | 255 us                                                                 | 252 us: 1.01x faster                                                 |
| json_dumps           | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                |
| pickle_pure_python   | 356 us                                                                 | 358 us: 1.00x slower                                                 |
| json_loads           | 29.4 us                                                                | 29.8 us: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 61.4 ms                                                                | 58.7 ms: 1.04x faster                                                |
| genshi_text     | 28.7 ms                                                                | 28.2 ms: 1.02x faster                                                |
| mako            | 16.0 ms                                                                | 15.9 ms: 1.00x faster                                                |
| django_template | 43.1 ms                                                                | 43.3 ms: 1.01x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8                   | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                                |
| pyflate                    | 516 ms                                                                 | 491 ms: 1.05x faster                                                 |
| nbody                      | 137 ms                                                                 | 131 ms: 1.05x faster                                                 |
| genshi_xml                 | 61.4 ms                                                                | 58.7 ms: 1.04x faster                                                |
| hexiom                     | 7.68 ms                                                                | 7.37 ms: 1.04x faster                                                |
| scimark_lu                 | 144 ms                                                                 | 139 ms: 1.04x faster                                                 |
| regex_compile              | 158 ms                                                                 | 152 ms: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                                 | 174 ms: 1.03x faster                                                 |
| scimark_fft                | 400 ms                                                                 | 388 ms: 1.03x faster                                                 |
| comprehensions             | 20.9 us                                                                | 20.3 us: 1.03x faster                                                |
| xml_etree_generate         | 98.3 ms                                                                | 95.5 ms: 1.03x faster                                                |
| thrift                     | 896 us                                                                 | 872 us: 1.03x faster                                                 |
| tomli_loads                | 2.35 sec                                                               | 2.29 sec: 1.03x faster                                               |
| scimark_sparse_mat_mult    | 5.83 ms                                                                | 5.69 ms: 1.02x faster                                                |
| scimark_sor                | 136 ms                                                                 | 132 ms: 1.02x faster                                                 |
| sqlalchemy_imperative      | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                                |
| xml_etree_process          | 71.2 ms                                                                | 69.6 ms: 1.02x faster                                                |
| async_generators           | 384 ms                                                                 | 375 ms: 1.02x faster                                                 |
| scimark_monte_carlo        | 84.2 ms                                                                | 82.3 ms: 1.02x faster                                                |
| many_optionals             | 1.18 ms                                                                | 1.15 ms: 1.02x faster                                                |
| go                         | 144 ms                                                                 | 141 ms: 1.02x faster                                                 |
| coroutines                 | 23.5 ms                                                                | 23.0 ms: 1.02x faster                                                |
| sympy_expand               | 558 ms                                                                 | 547 ms: 1.02x faster                                                 |
| chaos                      | 68.8 ms                                                                | 67.4 ms: 1.02x faster                                                |
| genshi_text                | 28.7 ms                                                                | 28.2 ms: 1.02x faster                                                |
| sympy_str                  | 338 ms                                                                 | 332 ms: 1.02x faster                                                 |
| subparsers                 | 25.6 ms                                                                | 25.2 ms: 1.02x faster                                                |
| meteor_contest             | 131 ms                                                                 | 129 ms: 1.02x faster                                                 |
| sqlglot_v2_transpile       | 1.94 ms                                                                | 1.91 ms: 1.02x faster                                                |
| typing_runtime_protocols   | 199 us                                                                 | 195 us: 1.02x faster                                                 |
| html5lib                   | 71.5 ms                                                                | 70.4 ms: 1.02x faster                                                |
| sympy_integrate            | 23.9 ms                                                                | 23.5 ms: 1.02x faster                                                |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                 |
| dulwich_log                | 73.3 ms                                                                | 72.2 ms: 1.02x faster                                                |
| logging_silent             | 114 ns                                                                 | 113 ns: 1.01x faster                                                 |
| logging_format             | 8.39 us                                                                | 8.27 us: 1.01x faster                                                |
| unpickle_pure_python       | 255 us                                                                 | 252 us: 1.01x faster                                                 |
| coverage                   | 109 ms                                                                 | 108 ms: 1.01x faster                                                 |
| spectral_norm              | 114 ms                                                                 | 112 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 158 ms                                                                 | 156 ms: 1.01x faster                                                 |
| connected_components       | 505 ms                                                                 | 499 ms: 1.01x faster                                                 |
| sympy_sum                  | 187 ms                                                                 | 185 ms: 1.01x faster                                                 |
| sqlglot_v2_optimize        | 61.4 ms                                                                | 60.8 ms: 1.01x faster                                                |
| sqlglot_v2_parse           | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                                |
| sqlglot_v2_normalize       | 121 ms                                                                 | 120 ms: 1.01x faster                                                 |
| shortest_path              | 548 ms                                                                 | 543 ms: 1.01x faster                                                 |
| richards                   | 55.0 ms                                                                | 54.5 ms: 1.01x faster                                                |
| logging_simple             | 7.39 us                                                                | 7.32 us: 1.01x faster                                                |
| pathlib                    | 20.1 ms                                                                | 20.0 ms: 1.01x faster                                                |
| mdp                        | 2.73 sec                                                               | 2.70 sec: 1.01x faster                                               |
| raytrace                   | 323 ms                                                                 | 320 ms: 1.01x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| fannkuch                   | 496 ms                                                                 | 492 ms: 1.01x faster                                                 |
| 2to3                       | 299 ms                                                                 | 297 ms: 1.01x faster                                                 |
| bench_mp_pool              | 97.3 ms                                                                | 96.6 ms: 1.01x faster                                                |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                |
| deepcopy                   | 315 us                                                                 | 313 us: 1.01x faster                                                 |
| json_dumps                 | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                |
| sphinx                     | 1.10 sec                                                               | 1.10 sec: 1.01x faster                                               |
| float                      | 76.8 ms                                                                | 76.4 ms: 1.00x faster                                                |
| deltablue                  | 3.86 ms                                                                | 3.85 ms: 1.00x faster                                                |
| pycparser                  | 1.19 sec                                                               | 1.18 sec: 1.00x faster                                               |
| mako                       | 16.0 ms                                                                | 15.9 ms: 1.00x faster                                                |
| bench_thread_pool          | 3.16 ms                                                                | 3.15 ms: 1.00x faster                                                |
| nqueens                    | 98.9 ms                                                                | 99.1 ms: 1.00x slower                                                |
| asyncio_websockets         | 517 ms                                                                 | 518 ms: 1.00x slower                                                 |
| pickle_pure_python         | 356 us                                                                 | 358 us: 1.00x slower                                                 |
| create_gc_cycles           | 1.37 ms                                                                | 1.38 ms: 1.01x slower                                                |
| django_template            | 43.1 ms                                                                | 43.3 ms: 1.01x slower                                                |
| pprint_safe_repr           | 837 ms                                                                 | 842 ms: 1.01x slower                                                 |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| async_tree_memoization     | 331 ms                                                                 | 334 ms: 1.01x slower                                                 |
| async_tree_io              | 582 ms                                                                 | 588 ms: 1.01x slower                                                 |
| json_loads                 | 29.4 us                                                                | 29.8 us: 1.01x slower                                                |
| deepcopy_reduce            | 3.24 us                                                                | 3.35 us: 1.03x slower                                                |
| generators                 | 32.0 ms                                                                | 33.3 ms: 1.04x slower                                                |
| regex_effbot               | 2.64 ms                                                                | 2.77 ms: 1.05x slower                                                |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 537 ms: 1.11x slower                                                 |
| async_tree_cpu_io_mixed    | 515 ms                                                                 | 572 ms: 1.11x slower                                                 |
| pidigits                   | 193 ms                                                                 | 223 ms: 1.15x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (16): pylint, sqlite_synth, bpe_tokeniser, k_core, richards_super, async_tree_none_tg, json, xml_etree_iterparse, docutils, telco, gc_traversal, crypto_pyaes, pprint_pformat, deepcopy_memo, async_tree_io_tg, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x