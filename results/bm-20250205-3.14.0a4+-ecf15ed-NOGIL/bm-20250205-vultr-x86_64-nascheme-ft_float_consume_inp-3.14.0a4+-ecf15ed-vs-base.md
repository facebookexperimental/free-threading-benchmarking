# Results vs. base

- fork: nascheme
- ref: ft_float_consume_inp
- machine: linux-x86_64
- commit hash: ecf15ed
- commit date: 2025-02-05
- overall geometric mean: 1.002x faster
- HPT reliability: 60.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 302 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 584 ms                                                                 | 533 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                 | 504 ms: 1.09x faster                                                     |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                                     |
| coroutines                 | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (7): async_tree_none, async_tree_memoization, asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 229 ms                                                                 | 198 ms: 1.16x faster                                                     |
| float          | 78.8 ms                                                                | 76.2 ms: 1.03x faster                                                    |
| nbody          | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 150 ms: 1.01x faster                                                     |
| regex_v8       | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                    |
| regex_dna      | 180 ms                                                                 | 182 ms: 1.01x slower                                                     |
| regex_effbot   | 2.69 ms                                                                | 2.79 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 31.5 us                                                                | 31.2 us: 1.01x faster                                                    |
| tomli_loads          | 2.35 sec                                                               | 2.34 sec: 1.01x faster                                                   |
| xml_etree_iterparse  | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                    |
| xml_etree_parse      | 128 ms                                                                 | 128 ms: 1.01x slower                                                     |
| unpickle_pure_python | 245 us                                                                 | 246 us: 1.01x slower                                                     |
| json_dumps           | 12.7 ms                                                                | 13.1 ms: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                                    |
| python_startup_no_site | 9.63 ms                                                                | 9.68 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 58.5 ms                                                                | 58.9 ms: 1.01x slower                                                    |
| genshi_text     | 27.5 ms                                                                | 27.8 ms: 1.01x slower                                                    |
| mako            | 15.7 ms                                                                | 16.0 ms: 1.02x slower                                                    |
| django_template | 41.8 ms                                                                | 42.7 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4+-7d9a22f | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 229 ms                                                                 | 198 ms: 1.16x faster                                                     |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.13 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 584 ms                                                                 | 533 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                 | 504 ms: 1.09x faster                                                     |
| spectral_norm              | 109 ms                                                                 | 105 ms: 1.04x faster                                                     |
| float                      | 78.8 ms                                                                | 76.2 ms: 1.03x faster                                                    |
| scimark_fft                | 391 ms                                                                 | 380 ms: 1.03x faster                                                     |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                   |
| scimark_lu                 | 137 ms                                                                 | 135 ms: 1.02x faster                                                     |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                                     |
| generators                 | 32.4 ms                                                                | 32.1 ms: 1.01x faster                                                    |
| json_loads                 | 31.5 us                                                                | 31.2 us: 1.01x faster                                                    |
| json                       | 5.45 ms                                                                | 5.40 ms: 1.01x faster                                                    |
| tomli_loads                | 2.35 sec                                                               | 2.34 sec: 1.01x faster                                                   |
| nbody                      | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| raytrace                   | 327 ms                                                                 | 325 ms: 1.01x faster                                                     |
| regex_compile              | 151 ms                                                                 | 150 ms: 1.01x faster                                                     |
| mdp                        | 2.71 sec                                                               | 2.69 sec: 1.01x faster                                                   |
| 2to3                       | 304 ms                                                                 | 302 ms: 1.00x faster                                                     |
| dulwich_log                | 82.0 ms                                                                | 81.6 ms: 1.00x faster                                                    |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                                    |
| go                         | 139 ms                                                                 | 139 ms: 1.00x faster                                                     |
| sympy_str                  | 334 ms                                                                 | 335 ms: 1.00x slower                                                     |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                                    |
| bpe_tokeniser              | 4.66 sec                                                               | 4.67 sec: 1.00x slower                                                   |
| create_gc_cycles           | 1.40 ms                                                                | 1.40 ms: 1.00x slower                                                    |
| nqueens                    | 96.0 ms                                                                | 96.5 ms: 1.01x slower                                                    |
| python_startup_no_site     | 9.63 ms                                                                | 9.68 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                    |
| xml_etree_parse            | 128 ms                                                                 | 128 ms: 1.01x slower                                                     |
| unpickle_pure_python       | 245 us                                                                 | 246 us: 1.01x slower                                                     |
| sympy_sum                  | 185 ms                                                                 | 187 ms: 1.01x slower                                                     |
| comprehensions             | 19.7 us                                                                | 19.8 us: 1.01x slower                                                    |
| pprint_safe_repr           | 803 ms                                                                 | 808 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.66 sec                                                               | 1.67 sec: 1.01x slower                                                   |
| genshi_xml                 | 58.5 ms                                                                | 58.9 ms: 1.01x slower                                                    |
| subparsers                 | 25.3 ms                                                                | 25.5 ms: 1.01x slower                                                    |
| genshi_text                | 27.5 ms                                                                | 27.8 ms: 1.01x slower                                                    |
| bench_thread_pool          | 3.29 ms                                                                | 3.32 ms: 1.01x slower                                                    |
| richards                   | 56.1 ms                                                                | 56.6 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 119 ms                                                                 | 120 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 3.15 us: 1.01x slower                                                    |
| fannkuch                   | 485 ms                                                                 | 491 ms: 1.01x slower                                                     |
| coroutines                 | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                    |
| regex_v8                   | 23.7 ms                                                                | 24.0 ms: 1.01x slower                                                    |
| meteor_contest             | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| richards_super             | 64.9 ms                                                                | 65.8 ms: 1.01x slower                                                    |
| gc_traversal               | 1.65 ms                                                                | 1.67 ms: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                                 | 182 ms: 1.01x slower                                                     |
| mako                       | 15.7 ms                                                                | 16.0 ms: 1.02x slower                                                    |
| deepcopy                   | 304 us                                                                 | 310 us: 1.02x slower                                                     |
| django_template            | 41.8 ms                                                                | 42.7 ms: 1.02x slower                                                    |
| pathlib                    | 18.3 ms                                                                | 18.7 ms: 1.02x slower                                                    |
| deltablue                  | 4.60 ms                                                                | 4.72 ms: 1.02x slower                                                    |
| crypto_pyaes               | 87.1 ms                                                                | 89.4 ms: 1.03x slower                                                    |
| json_dumps                 | 12.7 ms                                                                | 13.1 ms: 1.03x slower                                                    |
| regex_effbot               | 2.69 ms                                                                | 2.79 ms: 1.04x slower                                                    |
| pyflate                    | 490 ms                                                                 | 512 ms: 1.05x slower                                                     |
| logging_silent             | 109 ns                                                                 | 115 ns: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (37): logging_format, async_tree_none, thrift, sqlalchemy_imperative, pylint, sphinx, async_tree_memoization, scimark_monte_carlo, sqlalchemy_declarative, docutils, chaos, many_optionals, k_core, xml_etree_generate, hexiom, asyncio_websockets, deepcopy_memo, xml_etree_process, sympy_expand, async_tree_io, scimark_sor, logging_simple, sqlite_synth, sqlglot_transpile, html5lib, sqlglot_parse, shortest_path, telco, bench_mp_pool, coverage, sqlglot_optimize, typing_runtime_protocols, pickle_pure_python, async_tree_io_tg, connected_components, async_tree_memoization_tg, async_tree_none_tg

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 60.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x