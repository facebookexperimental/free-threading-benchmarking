# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 9015a3f
- commit date: 2024-12-18
- overall geometric mean: 1.023x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 364 ms                                                                 | 360 ms: 1.01x faster                                                     |
| docutils       | 3.05 sec                                                               | 3.03 sec: 1.01x faster                                                   |
| html5lib       | 96.0 ms                                                                | 93.2 ms: 1.03x faster                                                    |
| sphinx         | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 434 ms                                                                 | 401 ms: 1.08x faster                                                     |
| async_tree_none_tg         | 349 ms                                                                 | 322 ms: 1.08x faster                                                     |
| async_tree_memoization     | 464 ms                                                                 | 430 ms: 1.08x faster                                                     |
| async_tree_io_tg           | 793 ms                                                                 | 738 ms: 1.08x faster                                                     |
| async_tree_io              | 809 ms                                                                 | 762 ms: 1.06x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 354 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 605 ms                                                                 | 575 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 624 ms                                                                 | 598 ms: 1.04x faster                                                     |
| coroutines                 | 24.5 ms                                                                | 24.8 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 132 ms                                                                 | 114 ms: 1.16x faster                                                     |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                     |
| nbody          | 127 ms                                                                 | 129 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 175 ms                                                                 | 169 ms: 1.04x faster                                                     |
| regex_v8       | 24.8 ms                                                                | 24.1 ms: 1.03x faster                                                    |
| regex_effbot   | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| regex_dna      | 179 ms                                                                 | 184 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 78.1 ms                                                                | 75.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 339 us                                                                 | 329 us: 1.03x faster                                                     |
| xml_etree_iterparse  | 89.4 ms                                                                | 90.1 ms: 1.01x slower                                                    |
| xml_etree_generate   | 96.8 ms                                                                | 97.6 ms: 1.01x slower                                                    |
| json_dumps           | 13.9 ms                                                                | 14.1 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (4): pickle_pure_python, json_loads, tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.2 ms: 1.00x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 50.0 ms                                                                | 49.1 ms: 1.02x faster                                                    |
| mako            | 17.1 ms                                                                | 17.1 ms: 1.00x slower                                                    |
| genshi_xml      | 62.4 ms                                                                | 63.4 ms: 1.02x slower                                                    |
| genshi_text     | 30.0 ms                                                                | 30.6 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 132 ms                                                                 | 114 ms: 1.16x faster                                                     |
| richards                   | 77.0 ms                                                                | 68.5 ms: 1.12x faster                                                    |
| thrift                     | 1.09 ms                                                                | 977 us: 1.12x faster                                                     |
| richards_super             | 85.6 ms                                                                | 76.7 ms: 1.12x faster                                                    |
| raytrace                   | 548 ms                                                                 | 496 ms: 1.11x faster                                                     |
| logging_simple             | 10.0 us                                                                | 9.11 us: 1.10x faster                                                    |
| scimark_monte_carlo        | 118 ms                                                                 | 108 ms: 1.10x faster                                                     |
| pycparser                  | 1.52 sec                                                               | 1.39 sec: 1.10x faster                                                   |
| logging_format             | 11.0 us                                                                | 10.1 us: 1.09x faster                                                    |
| chaos                      | 104 ms                                                                 | 95.4 ms: 1.09x faster                                                    |
| go                         | 266 ms                                                                 | 245 ms: 1.09x faster                                                     |
| async_tree_memoization_tg  | 434 ms                                                                 | 401 ms: 1.08x faster                                                     |
| async_tree_none_tg         | 349 ms                                                                 | 322 ms: 1.08x faster                                                     |
| async_tree_memoization     | 464 ms                                                                 | 430 ms: 1.08x faster                                                     |
| sqlglot_parse              | 2.55 ms                                                                | 2.37 ms: 1.08x faster                                                    |
| async_tree_io_tg           | 793 ms                                                                 | 738 ms: 1.08x faster                                                     |
| sqlglot_transpile          | 2.92 ms                                                                | 2.73 ms: 1.07x faster                                                    |
| subparsers                 | 30.5 ms                                                                | 28.6 ms: 1.07x faster                                                    |
| deltablue                  | 8.14 ms                                                                | 7.66 ms: 1.06x faster                                                    |
| async_tree_io              | 809 ms                                                                 | 762 ms: 1.06x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 354 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 605 ms                                                                 | 575 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 624 ms                                                                 | 598 ms: 1.04x faster                                                     |
| dulwich_log                | 94.0 ms                                                                | 90.4 ms: 1.04x faster                                                    |
| xml_etree_process          | 78.1 ms                                                                | 75.4 ms: 1.04x faster                                                    |
| regex_compile              | 175 ms                                                                 | 169 ms: 1.04x faster                                                     |
| sqlalchemy_imperative      | 28.5 ms                                                                | 27.6 ms: 1.03x faster                                                    |
| unpickle_pure_python       | 339 us                                                                 | 329 us: 1.03x faster                                                     |
| html5lib                   | 96.0 ms                                                                | 93.2 ms: 1.03x faster                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.14 us: 1.03x faster                                                    |
| spectral_norm              | 115 ms                                                                 | 112 ms: 1.03x faster                                                     |
| sqlalchemy_declarative     | 201 ms                                                                 | 196 ms: 1.03x faster                                                     |
| regex_v8                   | 24.8 ms                                                                | 24.1 ms: 1.03x faster                                                    |
| many_optionals             | 1.26 ms                                                                | 1.23 ms: 1.02x faster                                                    |
| pathlib                    | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                                    |
| django_template            | 50.0 ms                                                                | 49.1 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 973 ms                                                                 | 954 ms: 1.02x faster                                                     |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.01x faster                                                     |
| pprint_pformat             | 2.02 sec                                                               | 1.99 sec: 1.01x faster                                                   |
| regex_effbot               | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| pyflate                    | 670 ms                                                                 | 663 ms: 1.01x faster                                                     |
| 2to3                       | 364 ms                                                                 | 360 ms: 1.01x faster                                                     |
| sphinx                     | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                   |
| docutils                   | 3.05 sec                                                               | 3.03 sec: 1.01x faster                                                   |
| nqueens                    | 99.0 ms                                                                | 98.2 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 3.41 us                                                                | 3.38 us: 1.01x faster                                                    |
| connected_components       | 500 ms                                                                 | 496 ms: 1.01x faster                                                     |
| hexiom                     | 9.86 ms                                                                | 9.82 ms: 1.00x faster                                                    |
| generators                 | 38.4 ms                                                                | 38.2 ms: 1.00x faster                                                    |
| sympy_sum                  | 349 ms                                                                 | 348 ms: 1.00x faster                                                     |
| python_startup             | 17.2 ms                                                                | 17.2 ms: 1.00x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                    |
| bpe_tokeniser              | 5.00 sec                                                               | 5.01 sec: 1.00x slower                                                   |
| mako                       | 17.1 ms                                                                | 17.1 ms: 1.00x slower                                                    |
| mdp                        | 2.79 sec                                                               | 2.80 sec: 1.01x slower                                                   |
| crypto_pyaes               | 89.7 ms                                                                | 90.4 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 89.4 ms                                                                | 90.1 ms: 1.01x slower                                                    |
| xml_etree_generate         | 96.8 ms                                                                | 97.6 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                 | 133 ms: 1.01x slower                                                     |
| meteor_contest             | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| coroutines                 | 24.5 ms                                                                | 24.8 ms: 1.01x slower                                                    |
| fannkuch                   | 489 ms                                                                 | 495 ms: 1.01x slower                                                     |
| scimark_lu                 | 180 ms                                                                 | 183 ms: 1.01x slower                                                     |
| json_dumps                 | 13.9 ms                                                                | 14.1 ms: 1.01x slower                                                    |
| logging_silent             | 185 ns                                                                 | 188 ns: 1.02x slower                                                     |
| genshi_xml                 | 62.4 ms                                                                | 63.4 ms: 1.02x slower                                                    |
| deepcopy_memo              | 39.9 us                                                                | 40.5 us: 1.02x slower                                                    |
| nbody                      | 127 ms                                                                 | 129 ms: 1.02x slower                                                     |
| genshi_text                | 30.0 ms                                                                | 30.6 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 203 us                                                                 | 207 us: 1.02x slower                                                     |
| scimark_fft                | 373 ms                                                                 | 383 ms: 1.02x slower                                                     |
| regex_dna                  | 179 ms                                                                 | 184 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult    | 5.39 ms                                                                | 5.80 ms: 1.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (23): pylint, json, scimark_sor, pickle_pure_python, telco, json_loads, sympy_str, sympy_expand, comprehensions, tomli_loads, bench_thread_pool, bench_mp_pool, sympy_integrate, sqlglot_optimize, k_core, async_generators, xml_etree_parse, gc_traversal, deepcopy, coverage, shortest_path, asyncio_websockets, create_gc_cycles

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x