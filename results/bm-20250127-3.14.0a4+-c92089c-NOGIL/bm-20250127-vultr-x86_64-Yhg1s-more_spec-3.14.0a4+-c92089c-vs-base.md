# Results vs. base

- fork: Yhg1s
- ref: more_spec
- machine: linux-x86_64
- commit hash: c92089c
- commit date: 2025-01-27
- overall geometric mean: 1.009x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 308 ms                                                                 | 307 ms: 1.00x faster                                       |
| docutils       | 2.86 sec                                                               | 2.83 sec: 1.01x faster                                     |
| html5lib       | 71.7 ms                                                                | 69.3 ms: 1.03x faster                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_generators        | 378 ms                                                                 | 372 ms: 1.02x faster                                       |
| async_tree_io           | 620 ms                                                                 | 616 ms: 1.01x faster                                       |
| async_tree_cpu_io_mixed | 542 ms                                                                 | 544 ms: 1.00x slower                                       |
| coroutines              | 24.2 ms                                                                | 24.4 ms: 1.01x slower                                      |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none, async_tree_none_tg, async_tree_memoization, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| nbody          | 141 ms                                                                 | 131 ms: 1.08x faster                                       |
| float          | 78.1 ms                                                                | 76.7 ms: 1.02x faster                                      |
| pidigits       | 197 ms                                                                 | 198 ms: 1.00x slower                                       |
| Geometric mean | (ref)                                                                  | 1.03x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 198 ms                                                                 | 184 ms: 1.08x faster                                       |
| regex_effbot   | 2.96 ms                                                                | 2.84 ms: 1.04x faster                                      |
| Geometric mean | (ref)                                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads         | 2.38 sec                                                               | 2.29 sec: 1.04x faster                                     |
| xml_etree_process   | 70.7 ms                                                                | 70.0 ms: 1.01x faster                                      |
| json_loads          | 31.1 us                                                                | 30.9 us: 1.01x faster                                      |
| json_dumps          | 13.0 ms                                                                | 12.9 ms: 1.00x faster                                      |
| pickle_pure_python  | 380 us                                                                 | 383 us: 1.01x slower                                       |
| xml_etree_iterparse | 87.8 ms                                                                | 88.5 ms: 1.01x slower                                      |
| xml_etree_parse     | 128 ms                                                                 | 130 ms: 1.01x slower                                       |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 28.6 ms                                                                | 27.8 ms: 1.03x faster                                      |
| genshi_xml      | 60.9 ms                                                                | 60.4 ms: 1.01x faster                                      |
| django_template | 44.4 ms                                                                | 44.5 ms: 1.00x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4+-a5075cd | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| nbody                   | 141 ms                                                                 | 131 ms: 1.08x faster                                       |
| regex_dna               | 198 ms                                                                 | 184 ms: 1.08x faster                                       |
| scimark_sparse_mat_mult | 5.87 ms                                                                | 5.47 ms: 1.07x faster                                      |
| scimark_fft             | 396 ms                                                                 | 379 ms: 1.04x faster                                       |
| regex_effbot            | 2.96 ms                                                                | 2.84 ms: 1.04x faster                                      |
| tomli_loads             | 2.38 sec                                                               | 2.29 sec: 1.04x faster                                     |
| html5lib                | 71.7 ms                                                                | 69.3 ms: 1.03x faster                                      |
| gc_traversal            | 3.25 ms                                                                | 3.15 ms: 1.03x faster                                      |
| mdp                     | 2.67 sec                                                               | 2.60 sec: 1.03x faster                                     |
| genshi_text             | 28.6 ms                                                                | 27.8 ms: 1.03x faster                                      |
| coverage                | 98.9 ms                                                                | 96.6 ms: 1.02x faster                                      |
| scimark_sor             | 135 ms                                                                 | 132 ms: 1.02x faster                                       |
| hexiom                  | 7.54 ms                                                                | 7.37 ms: 1.02x faster                                      |
| sqlalchemy_imperative   | 24.5 ms                                                                | 23.9 ms: 1.02x faster                                      |
| fannkuch                | 490 ms                                                                 | 481 ms: 1.02x faster                                       |
| spectral_norm           | 112 ms                                                                 | 110 ms: 1.02x faster                                       |
| scimark_monte_carlo     | 83.9 ms                                                                | 82.3 ms: 1.02x faster                                      |
| crypto_pyaes            | 88.3 ms                                                                | 86.6 ms: 1.02x faster                                      |
| float                   | 78.1 ms                                                                | 76.7 ms: 1.02x faster                                      |
| async_generators        | 378 ms                                                                 | 372 ms: 1.02x faster                                       |
| sqlglot_parse           | 1.61 ms                                                                | 1.58 ms: 1.02x faster                                      |
| sympy_expand            | 559 ms                                                                 | 550 ms: 1.02x faster                                       |
| scimark_lu              | 140 ms                                                                 | 137 ms: 1.02x faster                                       |
| logging_format          | 8.40 us                                                                | 8.26 us: 1.02x faster                                      |
| pprint_pformat          | 1.75 sec                                                               | 1.72 sec: 1.02x faster                                     |
| pprint_safe_repr        | 843 ms                                                                 | 830 ms: 1.02x faster                                       |
| sqlglot_transpile       | 1.94 ms                                                                | 1.91 ms: 1.02x faster                                      |
| deltablue               | 4.74 ms                                                                | 4.69 ms: 1.01x faster                                      |
| docutils                | 2.86 sec                                                               | 2.83 sec: 1.01x faster                                     |
| logging_simple          | 7.41 us                                                                | 7.33 us: 1.01x faster                                      |
| subparsers              | 26.0 ms                                                                | 25.7 ms: 1.01x faster                                      |
| pyflate                 | 498 ms                                                                 | 493 ms: 1.01x faster                                       |
| xml_etree_process       | 70.7 ms                                                                | 70.0 ms: 1.01x faster                                      |
| deepcopy_reduce         | 3.31 us                                                                | 3.28 us: 1.01x faster                                      |
| sympy_integrate         | 24.6 ms                                                                | 24.4 ms: 1.01x faster                                      |
| dulwich_log             | 83.0 ms                                                                | 82.2 ms: 1.01x faster                                      |
| comprehensions          | 21.1 us                                                                | 20.9 us: 1.01x faster                                      |
| sympy_str               | 340 ms                                                                 | 337 ms: 1.01x faster                                       |
| raytrace                | 333 ms                                                                 | 331 ms: 1.01x faster                                       |
| bpe_tokeniser           | 4.77 sec                                                               | 4.74 sec: 1.01x faster                                     |
| async_tree_io           | 620 ms                                                                 | 616 ms: 1.01x faster                                       |
| genshi_xml              | 60.9 ms                                                                | 60.4 ms: 1.01x faster                                      |
| sympy_sum               | 188 ms                                                                 | 187 ms: 1.01x faster                                       |
| json_loads              | 31.1 us                                                                | 30.9 us: 1.01x faster                                      |
| bench_thread_pool       | 3.34 ms                                                                | 3.32 ms: 1.01x faster                                      |
| pathlib                 | 19.0 ms                                                                | 18.8 ms: 1.01x faster                                      |
| chaos                   | 69.8 ms                                                                | 69.4 ms: 1.01x faster                                      |
| pycparser               | 1.21 sec                                                               | 1.20 sec: 1.01x faster                                     |
| json_dumps              | 13.0 ms                                                                | 12.9 ms: 1.00x faster                                      |
| many_optionals          | 1.19 ms                                                                | 1.19 ms: 1.00x faster                                      |
| sqlalchemy_declarative  | 165 ms                                                                 | 164 ms: 1.00x faster                                       |
| go                      | 140 ms                                                                 | 140 ms: 1.00x faster                                       |
| deepcopy                | 321 us                                                                 | 320 us: 1.00x faster                                       |
| 2to3                    | 308 ms                                                                 | 307 ms: 1.00x faster                                       |
| django_template         | 44.4 ms                                                                | 44.5 ms: 1.00x slower                                      |
| pidigits                | 197 ms                                                                 | 198 ms: 1.00x slower                                       |
| async_tree_cpu_io_mixed | 542 ms                                                                 | 544 ms: 1.00x slower                                       |
| pickle_pure_python      | 380 us                                                                 | 383 us: 1.01x slower                                       |
| xml_etree_iterparse     | 87.8 ms                                                                | 88.5 ms: 1.01x slower                                      |
| coroutines              | 24.2 ms                                                                | 24.4 ms: 1.01x slower                                      |
| create_gc_cycles        | 1.32 ms                                                                | 1.34 ms: 1.01x slower                                      |
| richards_super          | 66.0 ms                                                                | 66.9 ms: 1.01x slower                                      |
| sqlite_synth            | 2.06 us                                                                | 2.08 us: 1.01x slower                                      |
| xml_etree_parse         | 128 ms                                                                 | 130 ms: 1.01x slower                                       |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (32): pylint, meteor_contest, sphinx, async_tree_io_tg, async_tree_none, sqlglot_optimize, telco, nqueens, bench_mp_pool, richards, k_core, async_tree_none_tg, mako, unpickle_pure_python, thrift, regex_v8, sqlglot_normalize, async_tree_memoization, deepcopy_memo, python_startup, async_tree_memoization_tg, python_startup_no_site, generators, xml_etree_generate, logging_silent, asyncio_websockets, regex_compile, async_tree_cpu_io_mixed_tg, connected_components, json, shortest_path, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x