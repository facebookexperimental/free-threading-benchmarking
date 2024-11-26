# Results vs. base

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.002x faster
- HPT reliability: 70.21%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 570 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 568 ms: 1.10x faster                                                     |
| async_generators           | 370 ms                                                                 | 377 ms: 1.02x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 22.5 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (7): asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 185 ms: 1.18x faster                                                     |
| nbody          | 95.4 ms                                                                | 94.2 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                                 | 129 ms: 1.02x faster                                                     |
| regex_v8       | 23.4 ms                                                                | 24.0 ms: 1.03x slower                                                    |
| regex_effbot   | 2.75 ms                                                                | 2.87 ms: 1.04x slower                                                    |
| regex_dna      | 177 ms                                                                 | 186 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 11.7 ms                                                                | 11.4 ms: 1.02x faster                                                    |
| xml_etree_parse      | 138 ms                                                                 | 137 ms: 1.01x faster                                                     |
| json_loads           | 25.0 us                                                                | 24.8 us: 1.01x faster                                                    |
| unpickle_pure_python | 215 us                                                                 | 216 us: 1.00x slower                                                     |
| xml_etree_process    | 59.6 ms                                                                | 60.0 ms: 1.01x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                    |
| pickle_pure_python   | 314 us                                                                 | 321 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 36.2 ms                                                                | 35.8 ms: 1.01x faster                                                    |
| mako            | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                    |
| genshi_xml      | 50.4 ms                                                                | 50.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                                 | 185 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 570 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 568 ms: 1.10x faster                                                     |
| gc_traversal               | 4.45 ms                                                                | 4.24 ms: 1.05x faster                                                    |
| regex_compile              | 132 ms                                                                 | 129 ms: 1.02x faster                                                     |
| fannkuch                   | 385 ms                                                                 | 377 ms: 1.02x faster                                                     |
| json_dumps                 | 11.7 ms                                                                | 11.4 ms: 1.02x faster                                                    |
| nbody                      | 95.4 ms                                                                | 94.2 ms: 1.01x faster                                                    |
| django_template            | 36.2 ms                                                                | 35.8 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 160 us                                                                 | 158 us: 1.01x faster                                                     |
| create_gc_cycles           | 1.94 ms                                                                | 1.92 ms: 1.01x faster                                                    |
| crypto_pyaes               | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                    |
| sympy_str                  | 275 ms                                                                 | 273 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.72 ms                                                                | 4.69 ms: 1.01x faster                                                    |
| xml_etree_parse            | 138 ms                                                                 | 137 ms: 1.01x faster                                                     |
| json_loads                 | 25.0 us                                                                | 24.8 us: 1.01x faster                                                    |
| sqlite_synth               | 2.22 us                                                                | 2.21 us: 1.01x faster                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 126 ms: 1.01x faster                                                     |
| mako                       | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.42 sec                                                               | 4.40 sec: 1.00x faster                                                   |
| hexiom                     | 5.96 ms                                                                | 5.94 ms: 1.00x faster                                                    |
| scimark_fft                | 337 ms                                                                 | 336 ms: 1.00x faster                                                     |
| pprint_pformat             | 1.47 sec                                                               | 1.47 sec: 1.00x slower                                                   |
| unpickle_pure_python       | 215 us                                                                 | 216 us: 1.00x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                                | 53.6 ms: 1.01x slower                                                    |
| deepcopy                   | 260 us                                                                 | 262 us: 1.01x slower                                                     |
| many_optionals             | 1.02 ms                                                                | 1.02 ms: 1.01x slower                                                    |
| genshi_xml                 | 50.4 ms                                                                | 50.7 ms: 1.01x slower                                                    |
| pprint_safe_repr           | 716 ms                                                                 | 720 ms: 1.01x slower                                                     |
| pyflate                    | 446 ms                                                                 | 449 ms: 1.01x slower                                                     |
| xml_etree_process          | 59.6 ms                                                                | 60.0 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 107 ms: 1.01x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                    |
| pathlib                    | 18.3 ms                                                                | 18.5 ms: 1.01x slower                                                    |
| deepcopy_memo              | 30.3 us                                                                | 30.5 us: 1.01x slower                                                    |
| sympy_expand               | 457 ms                                                                 | 461 ms: 1.01x slower                                                     |
| raytrace                   | 263 ms                                                                 | 267 ms: 1.01x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 113 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 2.59 us                                                                | 2.63 us: 1.01x slower                                                    |
| logging_simple             | 6.20 us                                                                | 6.30 us: 1.02x slower                                                    |
| comprehensions             | 17.1 us                                                                | 17.5 us: 1.02x slower                                                    |
| async_generators           | 370 ms                                                                 | 377 ms: 1.02x slower                                                     |
| pickle_pure_python         | 314 us                                                                 | 321 us: 1.02x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 22.5 ms: 1.02x slower                                                    |
| coverage                   | 80.3 ms                                                                | 82.2 ms: 1.02x slower                                                    |
| logging_silent             | 105 ns                                                                 | 107 ns: 1.03x slower                                                     |
| logging_format             | 6.94 us                                                                | 7.13 us: 1.03x slower                                                    |
| regex_v8                   | 23.4 ms                                                                | 24.0 ms: 1.03x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 138 ms: 1.03x slower                                                     |
| regex_effbot               | 2.75 ms                                                                | 2.87 ms: 1.04x slower                                                    |
| regex_dna                  | 177 ms                                                                 | 186 ms: 1.05x slower                                                     |
| mdp                        | 2.36 sec                                                               | 2.50 sec: 1.06x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (43): meteor_contest, subparsers, shortest_path, telco, genshi_text, dulwich_log, connected_components, float, sympy_integrate, chaos, pylint, 2to3, pycparser, asyncio_websockets, python_startup_no_site, docutils, python_startup, xml_etree_iterparse, nqueens, bench_thread_pool, sqlglot_transpile, sympy_sum, async_tree_memoization, tomli_loads, json, async_tree_memoization_tg, richards, bench_mp_pool, scimark_monte_carlo, go, sqlalchemy_imperative, k_core, async_tree_none, sphinx, richards_super, spectral_norm, sqlglot_parse, generators, deltablue, thrift, async_tree_none_tg, async_tree_io, async_tree_io_tg

- Geometric mean (including insignificant results): 1.002x faster
# HPT report

- Reliability score: 70.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x