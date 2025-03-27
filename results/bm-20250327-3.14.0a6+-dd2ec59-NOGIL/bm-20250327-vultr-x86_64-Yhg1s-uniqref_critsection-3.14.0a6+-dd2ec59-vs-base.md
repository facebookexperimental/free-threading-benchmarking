# Results vs. base

- fork: Yhg1s
- ref: uniqref_critsection
- machine: linux-x86_64
- commit hash: dd2ec59
- commit date: 2025-03-27
- overall geometric mean: 1.006x slower
- HPT reliability: 87.94%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 301 ms: 1.01x slower                                                 |
| html5lib       | 71.5 ms                                                                | 72.2 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 553 ms                                                                 | 549 ms: 1.01x faster                                                 |
| async_generators           | 384 ms                                                                 | 387 ms: 1.01x slower                                                 |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 533 ms: 1.10x slower                                                 |
| async_tree_cpu_io_mixed    | 515 ms                                                                 | 567 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (5): async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.8 ms                                                                | 79.5 ms: 1.04x slower                                                |
| nbody          | 137 ms                                                                 | 143 ms: 1.04x slower                                                 |
| pidigits       | 193 ms                                                                 | 216 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                | 21.4 ms: 1.02x faster                                                |
| regex_compile  | 158 ms                                                                 | 157 ms: 1.00x faster                                                 |
| regex_effbot   | 2.64 ms                                                                | 2.77 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_generate   | 98.3 ms                                                                | 96.9 ms: 1.01x faster                                                |
| xml_etree_process    | 71.2 ms                                                                | 70.6 ms: 1.01x faster                                                |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                 |
| unpickle_pure_python | 255 us                                                                 | 258 us: 1.01x slower                                                 |
| tomli_loads          | 2.35 sec                                                               | 2.38 sec: 1.01x slower                                               |
| pickle_pure_python   | 356 us                                                                 | 363 us: 1.02x slower                                                 |
| json_loads           | 29.4 us                                                                | 30.5 us: 1.04x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (2): json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 61.4 ms                                                                | 60.0 ms: 1.02x faster                                                |
| genshi_text    | 28.7 ms                                                                | 28.5 ms: 1.01x faster                                                |
| mako           | 16.0 ms                                                                | 16.1 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250324-vultr-x86_64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| generators                 | 32.0 ms                                                                | 31.1 ms: 1.03x faster                                                |
| meteor_contest             | 131 ms                                                                 | 128 ms: 1.02x faster                                                 |
| genshi_xml                 | 61.4 ms                                                                | 60.0 ms: 1.02x faster                                                |
| pathlib                    | 20.1 ms                                                                | 19.7 ms: 1.02x faster                                                |
| subparsers                 | 25.6 ms                                                                | 25.2 ms: 1.02x faster                                                |
| mdp                        | 2.73 sec                                                               | 2.68 sec: 1.02x faster                                               |
| regex_v8                   | 21.7 ms                                                                | 21.4 ms: 1.02x faster                                                |
| telco                      | 9.03 ms                                                                | 8.89 ms: 1.02x faster                                                |
| xml_etree_generate         | 98.3 ms                                                                | 96.9 ms: 1.01x faster                                                |
| spectral_norm              | 114 ms                                                                 | 112 ms: 1.01x faster                                                 |
| coverage                   | 109 ms                                                                 | 108 ms: 1.01x faster                                                 |
| thrift                     | 896 us                                                                 | 884 us: 1.01x faster                                                 |
| sqlglot_v2_normalize       | 121 ms                                                                 | 120 ms: 1.01x faster                                                 |
| xml_etree_process          | 71.2 ms                                                                | 70.6 ms: 1.01x faster                                                |
| genshi_text                | 28.7 ms                                                                | 28.5 ms: 1.01x faster                                                |
| nqueens                    | 98.9 ms                                                                | 98.1 ms: 1.01x faster                                                |
| async_tree_io_tg           | 553 ms                                                                 | 549 ms: 1.01x faster                                                 |
| sympy_integrate            | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                |
| scimark_fft                | 400 ms                                                                 | 398 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 5.83 ms                                                                | 5.80 ms: 1.01x faster                                                |
| sympy_sum                  | 187 ms                                                                 | 186 ms: 1.01x faster                                                 |
| regex_compile              | 158 ms                                                                 | 157 ms: 1.00x faster                                                 |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                                |
| sympy_str                  | 338 ms                                                                 | 337 ms: 1.00x faster                                                 |
| pprint_safe_repr           | 837 ms                                                                 | 839 ms: 1.00x slower                                                 |
| k_core                     | 2.30 sec                                                               | 2.31 sec: 1.00x slower                                               |
| bench_thread_pool          | 3.16 ms                                                                | 3.17 ms: 1.00x slower                                                |
| comprehensions             | 20.9 us                                                                | 21.0 us: 1.00x slower                                                |
| bpe_tokeniser              | 4.86 sec                                                               | 4.88 sec: 1.00x slower                                               |
| logging_silent             | 114 ns                                                                 | 115 ns: 1.00x slower                                                 |
| mako                       | 16.0 ms                                                                | 16.1 ms: 1.01x slower                                                |
| scimark_lu                 | 144 ms                                                                 | 145 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.72 sec                                                               | 1.73 sec: 1.01x slower                                               |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                                 | 387 ms: 1.01x slower                                                 |
| 2to3                       | 299 ms                                                                 | 301 ms: 1.01x slower                                                 |
| pycparser                  | 1.19 sec                                                               | 1.20 sec: 1.01x slower                                               |
| chaos                      | 68.8 ms                                                                | 69.4 ms: 1.01x slower                                                |
| deepcopy                   | 315 us                                                                 | 318 us: 1.01x slower                                                 |
| scimark_monte_carlo        | 84.2 ms                                                                | 85.0 ms: 1.01x slower                                                |
| html5lib                   | 71.5 ms                                                                | 72.2 ms: 1.01x slower                                                |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| gc_traversal               | 1.81 ms                                                                | 1.83 ms: 1.01x slower                                                |
| fannkuch                   | 496 ms                                                                 | 501 ms: 1.01x slower                                                 |
| crypto_pyaes               | 88.1 ms                                                                | 88.9 ms: 1.01x slower                                                |
| unpickle_pure_python       | 255 us                                                                 | 258 us: 1.01x slower                                                 |
| dulwich_log                | 73.3 ms                                                                | 74.0 ms: 1.01x slower                                                |
| scimark_sor                | 136 ms                                                                 | 137 ms: 1.01x slower                                                 |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                                |
| sqlglot_v2_parse           | 1.59 ms                                                                | 1.61 ms: 1.01x slower                                                |
| deepcopy_memo              | 39.1 us                                                                | 39.5 us: 1.01x slower                                                |
| sqlite_synth               | 2.04 us                                                                | 2.07 us: 1.01x slower                                                |
| raytrace                   | 323 ms                                                                 | 327 ms: 1.01x slower                                                 |
| go                         | 144 ms                                                                 | 146 ms: 1.01x slower                                                 |
| tomli_loads                | 2.35 sec                                                               | 2.38 sec: 1.01x slower                                               |
| richards_super             | 63.9 ms                                                                | 64.9 ms: 1.02x slower                                                |
| create_gc_cycles           | 1.37 ms                                                                | 1.40 ms: 1.02x slower                                                |
| pickle_pure_python         | 356 us                                                                 | 363 us: 1.02x slower                                                 |
| richards                   | 55.0 ms                                                                | 56.1 ms: 1.02x slower                                                |
| typing_runtime_protocols   | 199 us                                                                 | 203 us: 1.02x slower                                                 |
| json                       | 5.13 ms                                                                | 5.26 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.24 us                                                                | 3.33 us: 1.03x slower                                                |
| float                      | 76.8 ms                                                                | 79.5 ms: 1.04x slower                                                |
| json_loads                 | 29.4 us                                                                | 30.5 us: 1.04x slower                                                |
| nbody                      | 137 ms                                                                 | 143 ms: 1.04x slower                                                 |
| regex_effbot               | 2.64 ms                                                                | 2.77 ms: 1.05x slower                                                |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 533 ms: 1.10x slower                                                 |
| async_tree_cpu_io_mixed    | 515 ms                                                                 | 567 ms: 1.10x slower                                                 |
| pidigits                   | 193 ms                                                                 | 216 ms: 1.12x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (26): pylint, shortest_path, logging_simple, sqlglot_v2_optimize, sqlalchemy_declarative, bench_mp_pool, sphinx, async_tree_memoization_tg, asyncio_websockets, pyflate, deltablue, sympy_expand, async_tree_none_tg, regex_dna, django_template, logging_format, hexiom, json_dumps, many_optionals, docutils, async_tree_memoization, async_tree_io, connected_components, xml_etree_iterparse, sqlalchemy_imperative, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 87.94% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x