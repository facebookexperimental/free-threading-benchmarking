# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 360 ms: 1.01x faster                                                     |
| docutils       | 3.08 sec                                                               | 3.05 sec: 1.01x faster                                                   |
| html5lib       | 98.4 ms                                                                | 95.0 ms: 1.04x faster                                                    |
| sphinx         | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 434 ms                                                                 | 401 ms: 1.08x faster                                                     |
| async_tree_none_tg         | 347 ms                                                                 | 322 ms: 1.08x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 429 ms: 1.08x faster                                                     |
| async_tree_io_tg           | 793 ms                                                                 | 740 ms: 1.07x faster                                                     |
| async_tree_io              | 813 ms                                                                 | 761 ms: 1.07x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 354 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 574 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 598 ms: 1.05x faster                                                     |
| coroutines                 | 25.2 ms                                                                | 24.1 ms: 1.05x faster                                                    |
| async_generators           | 453 ms                                                                 | 444 ms: 1.02x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 111 ms: 1.23x faster                                                     |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| nbody          | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 170 ms: 1.04x faster                                                     |
| regex_effbot   | 2.82 ms                                                                | 2.97 ms: 1.05x slower                                                    |
| regex_v8       | 23.7 ms                                                                | 25.0 ms: 1.06x slower                                                    |
| regex_dna      | 181 ms                                                                 | 192 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 79.0 ms                                                                | 73.8 ms: 1.07x faster                                                    |
| unpickle_pure_python | 335 us                                                                 | 331 us: 1.01x faster                                                     |
| xml_etree_generate   | 98.3 ms                                                                | 97.6 ms: 1.01x faster                                                    |
| xml_etree_iterparse  | 90.7 ms                                                                | 90.4 ms: 1.00x faster                                                    |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| json_dumps           | 14.0 ms                                                                | 14.2 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 17.2 ms                                                                | 17.2 ms: 1.00x faster                                                    |
| genshi_xml      | 63.2 ms                                                                | 63.7 ms: 1.01x slower                                                    |
| genshi_text     | 30.5 ms                                                                | 30.9 ms: 1.01x slower                                                    |
| django_template | 49.5 ms                                                                | 50.2 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 136 ms                                                                 | 111 ms: 1.23x faster                                                     |
| raytrace                   | 555 ms                                                                 | 495 ms: 1.12x faster                                                     |
| richards                   | 77.4 ms                                                                | 69.1 ms: 1.12x faster                                                    |
| gc_traversal               | 3.52 ms                                                                | 3.15 ms: 1.12x faster                                                    |
| sqlglot_parse              | 2.59 ms                                                                | 2.33 ms: 1.11x faster                                                    |
| thrift                     | 1.11 ms                                                                | 1.00 ms: 1.11x faster                                                    |
| richards_super             | 86.0 ms                                                                | 77.6 ms: 1.11x faster                                                    |
| pycparser                  | 1.54 sec                                                               | 1.39 sec: 1.11x faster                                                   |
| logging_simple             | 10.00 us                                                               | 9.06 us: 1.10x faster                                                    |
| sqlglot_transpile          | 2.95 ms                                                                | 2.69 ms: 1.10x faster                                                    |
| go                         | 268 ms                                                                 | 244 ms: 1.10x faster                                                     |
| scimark_monte_carlo        | 118 ms                                                                 | 108 ms: 1.10x faster                                                     |
| logging_format             | 11.1 us                                                                | 10.1 us: 1.09x faster                                                    |
| chaos                      | 104 ms                                                                 | 95.9 ms: 1.09x faster                                                    |
| async_tree_memoization_tg  | 434 ms                                                                 | 401 ms: 1.08x faster                                                     |
| async_tree_none_tg         | 347 ms                                                                 | 322 ms: 1.08x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 429 ms: 1.08x faster                                                     |
| async_tree_io_tg           | 793 ms                                                                 | 740 ms: 1.07x faster                                                     |
| deltablue                  | 8.19 ms                                                                | 7.65 ms: 1.07x faster                                                    |
| xml_etree_process          | 79.0 ms                                                                | 73.8 ms: 1.07x faster                                                    |
| async_tree_io              | 813 ms                                                                 | 761 ms: 1.07x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 354 ms: 1.06x faster                                                     |
| subparsers                 | 30.7 ms                                                                | 29.2 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 574 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 598 ms: 1.05x faster                                                     |
| coroutines                 | 25.2 ms                                                                | 24.1 ms: 1.05x faster                                                    |
| sqlalchemy_imperative      | 29.0 ms                                                                | 27.8 ms: 1.04x faster                                                    |
| regex_compile              | 177 ms                                                                 | 170 ms: 1.04x faster                                                     |
| html5lib                   | 98.4 ms                                                                | 95.0 ms: 1.04x faster                                                    |
| dulwich_log                | 93.9 ms                                                                | 90.8 ms: 1.03x faster                                                    |
| create_gc_cycles           | 1.83 ms                                                                | 1.78 ms: 1.03x faster                                                    |
| sqlalchemy_declarative     | 202 ms                                                                 | 196 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.21 us                                                                | 2.16 us: 1.02x faster                                                    |
| pprint_pformat             | 2.04 sec                                                               | 2.00 sec: 1.02x faster                                                   |
| async_generators           | 453 ms                                                                 | 444 ms: 1.02x faster                                                     |
| spectral_norm              | 112 ms                                                                 | 110 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 979 ms                                                                 | 965 ms: 1.02x faster                                                     |
| many_optionals             | 1.26 ms                                                                | 1.24 ms: 1.01x faster                                                    |
| pyflate                    | 671 ms                                                                 | 662 ms: 1.01x faster                                                     |
| coverage                   | 101 ms                                                                 | 99.2 ms: 1.01x faster                                                    |
| mdp                        | 2.90 sec                                                               | 2.86 sec: 1.01x faster                                                   |
| 2to3                       | 365 ms                                                                 | 360 ms: 1.01x faster                                                     |
| deepcopy_reduce            | 3.46 us                                                                | 3.42 us: 1.01x faster                                                    |
| unpickle_pure_python       | 335 us                                                                 | 331 us: 1.01x faster                                                     |
| scimark_sor                | 235 ms                                                                 | 232 ms: 1.01x faster                                                     |
| comprehensions             | 28.0 us                                                                | 27.7 us: 1.01x faster                                                    |
| sympy_str                  | 478 ms                                                                 | 473 ms: 1.01x faster                                                     |
| bench_mp_pool              | 108 ms                                                                 | 107 ms: 1.01x faster                                                     |
| docutils                   | 3.08 sec                                                               | 3.05 sec: 1.01x faster                                                   |
| sphinx                     | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                   |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| bench_thread_pool          | 3.40 ms                                                                | 3.37 ms: 1.01x faster                                                    |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| xml_etree_generate         | 98.3 ms                                                                | 97.6 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 66.2 ms                                                                | 65.7 ms: 1.01x faster                                                    |
| sympy_expand               | 958 ms                                                                 | 953 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 5.64 ms                                                                | 5.62 ms: 1.00x faster                                                    |
| sympy_integrate            | 29.5 ms                                                                | 29.4 ms: 1.00x faster                                                    |
| sympy_sum                  | 349 ms                                                                 | 348 ms: 1.00x faster                                                     |
| xml_etree_iterparse        | 90.7 ms                                                                | 90.4 ms: 1.00x faster                                                    |
| mako                       | 17.2 ms                                                                | 17.2 ms: 1.00x faster                                                    |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| bpe_tokeniser              | 5.02 sec                                                               | 5.03 sec: 1.00x slower                                                   |
| fannkuch                   | 496 ms                                                                 | 498 ms: 1.00x slower                                                     |
| scimark_lu                 | 184 ms                                                                 | 185 ms: 1.00x slower                                                     |
| hexiom                     | 9.83 ms                                                                | 9.87 ms: 1.00x slower                                                    |
| nqueens                    | 97.2 ms                                                                | 97.6 ms: 1.00x slower                                                    |
| telco                      | 8.60 ms                                                                | 8.64 ms: 1.01x slower                                                    |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| genshi_xml                 | 63.2 ms                                                                | 63.7 ms: 1.01x slower                                                    |
| deepcopy_memo              | 40.4 us                                                                | 40.8 us: 1.01x slower                                                    |
| deepcopy                   | 320 us                                                                 | 323 us: 1.01x slower                                                     |
| json                       | 5.02 ms                                                                | 5.07 ms: 1.01x slower                                                    |
| pathlib                    | 19.7 ms                                                                | 19.9 ms: 1.01x slower                                                    |
| json_dumps                 | 14.0 ms                                                                | 14.2 ms: 1.01x slower                                                    |
| genshi_text                | 30.5 ms                                                                | 30.9 ms: 1.01x slower                                                    |
| django_template            | 49.5 ms                                                                | 50.2 ms: 1.01x slower                                                    |
| scimark_fft                | 385 ms                                                                 | 392 ms: 1.02x slower                                                     |
| logging_silent             | 182 ns                                                                 | 186 ns: 1.02x slower                                                     |
| nbody                      | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| regex_effbot               | 2.82 ms                                                                | 2.97 ms: 1.05x slower                                                    |
| regex_v8                   | 23.7 ms                                                                | 25.0 ms: 1.06x slower                                                    |
| regex_dna                  | 181 ms                                                                 | 192 ms: 1.06x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (13): pylint, connected_components, meteor_contest, tomli_loads, generators, asyncio_websockets, json_loads, shortest_path, pickle_pure_python, k_core, typing_runtime_protocols, crypto_pyaes, sqlglot_normalize

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x