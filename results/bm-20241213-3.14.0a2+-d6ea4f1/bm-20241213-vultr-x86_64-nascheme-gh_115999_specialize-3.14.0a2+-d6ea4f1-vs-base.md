# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| docutils       | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| sphinx         | 980 ms                                                                 | 990 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg | 305 ms                                                                 | 308 ms: 1.01x slower                                                     |
| async_tree_none_tg        | 255 ms                                                                 | 257 ms: 1.01x slower                                                     |
| async_generators          | 359 ms                                                                 | 363 ms: 1.01x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (8): async_tree_none, async_tree_io_tg, asyncio_websockets, coroutines, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 217 ms: 1.00x slower                                                     |
| nbody          | 89.4 ms                                                                | 94.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 23.3 ms: 1.05x faster                                                    |
| regex_dna      | 172 ms                                                                 | 166 ms: 1.03x faster                                                     |
| regex_effbot   | 2.68 ms                                                                | 2.73 ms: 1.02x slower                                                    |
| regex_compile  | 127 ms                                                                 | 130 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 314 us                                                                 | 310 us: 1.01x faster                                                     |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.00x slower                                                     |
| json_dumps           | 11.3 ms                                                                | 11.4 ms: 1.00x slower                                                    |
| json_loads           | 26.5 us                                                                | 26.7 us: 1.01x slower                                                    |
| xml_etree_generate   | 82.9 ms                                                                | 84.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 57.8 ms                                                                | 58.7 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.47 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 49.8 ms: 1.01x slower                                                    |
| genshi_text     | 21.4 ms                                                                | 21.8 ms: 1.02x slower                                                    |
| django_template | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                    |
| mako            | 11.4 ms                                                                | 11.7 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal              | 4.62 ms                                                                | 4.25 ms: 1.09x faster                                                    |
| regex_v8                  | 24.5 ms                                                                | 23.3 ms: 1.05x faster                                                    |
| regex_dna                 | 172 ms                                                                 | 166 ms: 1.03x faster                                                     |
| logging_silent            | 106 ns                                                                 | 103 ns: 1.03x faster                                                     |
| pprint_pformat            | 1.45 sec                                                               | 1.42 sec: 1.02x faster                                                   |
| pprint_safe_repr          | 708 ms                                                                 | 699 ms: 1.01x faster                                                     |
| meteor_contest            | 100 ms                                                                 | 98.8 ms: 1.01x faster                                                    |
| pickle_pure_python        | 314 us                                                                 | 310 us: 1.01x faster                                                     |
| logging_format            | 6.78 us                                                                | 6.70 us: 1.01x faster                                                    |
| fannkuch                  | 375 ms                                                                 | 371 ms: 1.01x faster                                                     |
| deepcopy_reduce           | 2.60 us                                                                | 2.57 us: 1.01x faster                                                    |
| pathlib                   | 18.4 ms                                                                | 18.2 ms: 1.01x faster                                                    |
| crypto_pyaes              | 68.0 ms                                                                | 67.4 ms: 1.01x faster                                                    |
| deepcopy_memo             | 29.7 us                                                                | 29.4 us: 1.01x faster                                                    |
| xml_etree_parse           | 128 ms                                                                 | 127 ms: 1.01x faster                                                     |
| chaos                     | 57.5 ms                                                                | 57.2 ms: 1.00x faster                                                    |
| bench_thread_pool         | 1.03 ms                                                                | 1.02 ms: 1.00x faster                                                    |
| nqueens                   | 78.8 ms                                                                | 78.5 ms: 1.00x faster                                                    |
| python_startup            | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site    | 7.47 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| pidigits                  | 216 ms                                                                 | 217 ms: 1.00x slower                                                     |
| unpickle_pure_python      | 208 us                                                                 | 209 us: 1.00x slower                                                     |
| json_dumps                | 11.3 ms                                                                | 11.4 ms: 1.00x slower                                                    |
| many_optionals            | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 305 ms                                                                 | 308 ms: 1.01x slower                                                     |
| scimark_sor               | 131 ms                                                                 | 132 ms: 1.01x slower                                                     |
| 2to3                      | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| bpe_tokeniser             | 4.23 sec                                                               | 4.26 sec: 1.01x slower                                                   |
| async_tree_none_tg        | 255 ms                                                                 | 257 ms: 1.01x slower                                                     |
| deepcopy                  | 252 us                                                                 | 254 us: 1.01x slower                                                     |
| coverage                  | 78.1 ms                                                                | 78.8 ms: 1.01x slower                                                    |
| genshi_xml                | 49.3 ms                                                                | 49.8 ms: 1.01x slower                                                    |
| sympy_sum                 | 151 ms                                                                 | 153 ms: 1.01x slower                                                     |
| async_generators          | 359 ms                                                                 | 363 ms: 1.01x slower                                                     |
| sqlglot_optimize          | 51.7 ms                                                                | 52.2 ms: 1.01x slower                                                    |
| sphinx                    | 980 ms                                                                 | 990 ms: 1.01x slower                                                     |
| docutils                  | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| json_loads                | 26.5 us                                                                | 26.7 us: 1.01x slower                                                    |
| raytrace                  | 259 ms                                                                 | 261 ms: 1.01x slower                                                     |
| sqlglot_normalize         | 103 ms                                                                 | 104 ms: 1.01x slower                                                     |
| spectral_norm             | 108 ms                                                                 | 109 ms: 1.01x slower                                                     |
| json                      | 4.81 ms                                                                | 4.87 ms: 1.01x slower                                                    |
| scimark_monte_carlo       | 63.7 ms                                                                | 64.5 ms: 1.01x slower                                                    |
| xml_etree_generate        | 82.9 ms                                                                | 84.0 ms: 1.01x slower                                                    |
| sqlite_synth              | 2.23 us                                                                | 2.27 us: 1.01x slower                                                    |
| dulwich_log               | 74.8 ms                                                                | 75.9 ms: 1.01x slower                                                    |
| genshi_text               | 21.4 ms                                                                | 21.8 ms: 1.02x slower                                                    |
| comprehensions            | 17.0 us                                                                | 17.2 us: 1.02x slower                                                    |
| xml_etree_process         | 57.8 ms                                                                | 58.7 ms: 1.02x slower                                                    |
| generators                | 26.6 ms                                                                | 27.1 ms: 1.02x slower                                                    |
| sympy_str                 | 268 ms                                                                 | 273 ms: 1.02x slower                                                     |
| regex_effbot              | 2.68 ms                                                                | 2.73 ms: 1.02x slower                                                    |
| django_template           | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                    |
| sympy_integrate           | 19.6 ms                                                                | 20.0 ms: 1.02x slower                                                    |
| sqlglot_transpile         | 1.57 ms                                                                | 1.60 ms: 1.02x slower                                                    |
| typing_runtime_protocols  | 154 us                                                                 | 158 us: 1.02x slower                                                     |
| mako                      | 11.4 ms                                                                | 11.7 ms: 1.02x slower                                                    |
| regex_compile             | 127 ms                                                                 | 130 ms: 1.02x slower                                                     |
| sympy_expand              | 451 ms                                                                 | 461 ms: 1.02x slower                                                     |
| sqlglot_parse             | 1.26 ms                                                                | 1.29 ms: 1.02x slower                                                    |
| subparsers                | 21.5 ms                                                                | 22.1 ms: 1.03x slower                                                    |
| scimark_lu                | 107 ms                                                                 | 111 ms: 1.03x slower                                                     |
| sqlalchemy_imperative     | 18.8 ms                                                                | 19.4 ms: 1.03x slower                                                    |
| sqlalchemy_declarative    | 126 ms                                                                 | 131 ms: 1.04x slower                                                     |
| nbody                     | 89.4 ms                                                                | 94.2 ms: 1.05x slower                                                    |
| mdp                       | 2.34 sec                                                               | 2.48 sec: 1.06x slower                                                   |
| scimark_fft               | 323 ms                                                                 | 343 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult   | 4.37 ms                                                                | 4.89 ms: 1.12x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (27): create_gc_cycles, async_tree_none, go, deltablue, async_tree_io_tg, richards_super, telco, bench_mp_pool, shortest_path, pycparser, thrift, hexiom, asyncio_websockets, coroutines, connected_components, async_tree_cpu_io_mixed, richards, float, xml_etree_iterparse, async_tree_io, pyflate, async_tree_cpu_io_mixed_tg, tomli_loads, k_core, logging_simple, async_tree_memoization, pylint

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x