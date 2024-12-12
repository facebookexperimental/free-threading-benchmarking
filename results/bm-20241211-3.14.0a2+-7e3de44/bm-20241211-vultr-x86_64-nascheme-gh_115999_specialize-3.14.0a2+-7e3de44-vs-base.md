# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 7e3de44
- commit date: 2024-12-11
- overall geometric mean: 1.019x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| docutils       | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| sphinx         | 980 ms                                                                 | 994 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                    |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.02x slower                                                     |
| async_generators           | 359 ms                                                                 | 366 ms: 1.02x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 624 ms: 1.02x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 341 ms: 1.03x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 314 ms: 1.03x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 264 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 606 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 589 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.2 ms                                                                | 75.7 ms: 1.02x faster                                                    |
| nbody          | 89.4 ms                                                                | 90.5 ms: 1.01x slower                                                    |
| pidigits       | 216 ms                                                                 | 222 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                 | 171 ms: 1.00x faster                                                     |
| regex_compile  | 127 ms                                                                 | 133 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                                | 26.1 us: 1.02x faster                                                    |
| pickle_pure_python   | 314 us                                                                 | 311 us: 1.01x faster                                                     |
| xml_etree_generate   | 82.9 ms                                                                | 83.3 ms: 1.00x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 214 us: 1.03x slower                                                     |
| xml_etree_process    | 57.8 ms                                                                | 61.1 ms: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (4): tomli_loads, json_dumps, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.47 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                    |
| genshi_xml      | 49.3 ms                                                                | 50.5 ms: 1.02x slower                                                    |
| django_template | 34.6 ms                                                                | 35.7 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.62 ms                                                                | 4.27 ms: 1.08x faster                                                    |
| crypto_pyaes               | 68.0 ms                                                                | 66.7 ms: 1.02x faster                                                    |
| float                      | 77.2 ms                                                                | 75.7 ms: 1.02x faster                                                    |
| comprehensions             | 17.0 us                                                                | 16.7 us: 1.02x faster                                                    |
| json_loads                 | 26.5 us                                                                | 26.1 us: 1.02x faster                                                    |
| nqueens                    | 78.8 ms                                                                | 77.7 ms: 1.01x faster                                                    |
| json                       | 4.81 ms                                                                | 4.74 ms: 1.01x faster                                                    |
| meteor_contest             | 100 ms                                                                 | 98.8 ms: 1.01x faster                                                    |
| pprint_pformat             | 1.45 sec                                                               | 1.43 sec: 1.01x faster                                                   |
| pprint_safe_repr           | 708 ms                                                                 | 700 ms: 1.01x faster                                                     |
| pickle_pure_python         | 314 us                                                                 | 311 us: 1.01x faster                                                     |
| deepcopy_memo              | 29.7 us                                                                | 29.4 us: 1.01x faster                                                    |
| pathlib                    | 18.4 ms                                                                | 18.3 ms: 1.01x faster                                                    |
| deepcopy                   | 252 us                                                                 | 251 us: 1.01x faster                                                     |
| fannkuch                   | 375 ms                                                                 | 373 ms: 1.01x faster                                                     |
| regex_dna                  | 172 ms                                                                 | 171 ms: 1.00x faster                                                     |
| python_startup_no_site     | 7.47 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| xml_etree_generate         | 82.9 ms                                                                | 83.3 ms: 1.00x slower                                                    |
| bpe_tokeniser              | 4.23 sec                                                               | 4.25 sec: 1.01x slower                                                   |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.01x slower                                                    |
| coroutines                 | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 51.7 ms                                                                | 52.1 ms: 1.01x slower                                                    |
| 2to3                       | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 104 ms: 1.01x slower                                                     |
| sympy_sum                  | 151 ms                                                                 | 153 ms: 1.01x slower                                                     |
| docutils                   | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| sympy_str                  | 268 ms                                                                 | 271 ms: 1.01x slower                                                     |
| hexiom                     | 5.78 ms                                                                | 5.84 ms: 1.01x slower                                                    |
| nbody                      | 89.4 ms                                                                | 90.5 ms: 1.01x slower                                                    |
| sympy_expand               | 451 ms                                                                 | 456 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 154 us                                                                 | 156 us: 1.01x slower                                                     |
| sympy_integrate            | 19.6 ms                                                                | 19.9 ms: 1.01x slower                                                    |
| sphinx                     | 980 ms                                                                 | 994 ms: 1.01x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.02x slower                                                     |
| mako                       | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                    |
| generators                 | 26.6 ms                                                                | 27.1 ms: 1.02x slower                                                    |
| coverage                   | 78.1 ms                                                                | 79.5 ms: 1.02x slower                                                    |
| async_generators           | 359 ms                                                                 | 366 ms: 1.02x slower                                                     |
| sqlalchemy_imperative      | 18.8 ms                                                                | 19.2 ms: 1.02x slower                                                    |
| scimark_fft                | 323 ms                                                                 | 330 ms: 1.02x slower                                                     |
| sqlalchemy_declarative     | 126 ms                                                                 | 128 ms: 1.02x slower                                                     |
| dulwich_log                | 74.8 ms                                                                | 76.5 ms: 1.02x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 624 ms: 1.02x slower                                                     |
| deepcopy_reduce            | 2.60 us                                                                | 2.66 us: 1.02x slower                                                    |
| genshi_xml                 | 49.3 ms                                                                | 50.5 ms: 1.02x slower                                                    |
| pidigits                   | 216 ms                                                                 | 222 ms: 1.02x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 341 ms: 1.03x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 214 us: 1.03x slower                                                     |
| pyflate                    | 439 ms                                                                 | 450 ms: 1.03x slower                                                     |
| many_optionals             | 1.01 ms                                                                | 1.04 ms: 1.03x slower                                                    |
| django_template            | 34.6 ms                                                                | 35.7 ms: 1.03x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 314 ms: 1.03x slower                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 264 ms: 1.04x slower                                                     |
| regex_compile              | 127 ms                                                                 | 133 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 4.60 ms: 1.05x slower                                                    |
| xml_etree_process          | 57.8 ms                                                                | 61.1 ms: 1.06x slower                                                    |
| subparsers                 | 21.5 ms                                                                | 22.8 ms: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.06x slower                                                   |
| chaos                      | 57.5 ms                                                                | 61.1 ms: 1.06x slower                                                    |
| logging_format             | 6.78 us                                                                | 7.21 us: 1.06x slower                                                    |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 606 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 589 ms: 1.08x slower                                                     |
| logging_simple             | 5.95 us                                                                | 6.46 us: 1.09x slower                                                    |
| scimark_monte_carlo        | 63.7 ms                                                                | 70.5 ms: 1.11x slower                                                    |
| raytrace                   | 259 ms                                                                 | 291 ms: 1.12x slower                                                     |
| thrift                     | 726 us                                                                 | 816 us: 1.12x slower                                                     |
| go                         | 117 ms                                                                 | 132 ms: 1.13x slower                                                     |
| deltablue                  | 3.16 ms                                                                | 3.58 ms: 1.13x slower                                                    |
| richards_super             | 51.3 ms                                                                | 58.4 ms: 1.14x slower                                                    |
| richards                   | 45.3 ms                                                                | 52.0 ms: 1.15x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (24): create_gc_cycles, shortest_path, sqlglot_transpile, tomli_loads, sqlglot_parse, bench_mp_pool, mdp, json_dumps, xml_etree_iterparse, asyncio_websockets, xml_etree_parse, regex_effbot, scimark_sor, logging_silent, spectral_norm, genshi_text, k_core, connected_components, scimark_lu, telco, sqlite_synth, regex_v8, async_tree_io, pylint

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x