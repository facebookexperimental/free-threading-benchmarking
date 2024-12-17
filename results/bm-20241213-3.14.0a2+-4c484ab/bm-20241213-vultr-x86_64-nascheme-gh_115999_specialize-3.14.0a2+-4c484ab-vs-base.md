# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.006x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 256 ms: 1.00x slower                                                     |
| sphinx         | 992 ms                                                                 | 998 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 352 ms                                                                 | 354 ms: 1.00x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 619 ms: 1.01x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.01x slower                                                     |
| coroutines                 | 21.6 ms                                                                | 21.9 ms: 1.02x slower                                                    |
| async_tree_memoization     | 332 ms                                                                 | 337 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 550 ms: 1.14x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 572 ms: 1.14x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_io, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 90.3 ms                                                                | 89.2 ms: 1.01x faster                                                    |
| pidigits       | 185 ms                                                                 | 216 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 166 ms: 1.05x faster                                                     |
| regex_v8       | 24.4 ms                                                                | 23.5 ms: 1.04x faster                                                    |
| regex_effbot   | 2.69 ms                                                                | 2.74 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 323 us                                                                 | 318 us: 1.02x faster                                                     |
| unpickle_pure_python | 213 us                                                                 | 213 us: 1.00x slower                                                     |
| tomli_loads          | 1.97 sec                                                               | 1.98 sec: 1.00x slower                                                   |
| xml_etree_iterparse  | 90.6 ms                                                                | 91.3 ms: 1.01x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (4): xml_etree_process, xml_etree_generate, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.49 ms                                                                | 7.52 ms: 1.00x slower                                                    |
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 35.4 ms                                                                | 35.0 ms: 1.01x faster                                                    |
| mako            | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| genshi_xml      | 49.7 ms                                                                | 50.6 ms: 1.02x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                | 4.04 ms: 1.06x faster                                                    |
| regex_dna                  | 175 ms                                                                 | 166 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 4.20 ms: 1.04x faster                                                    |
| regex_v8                   | 24.4 ms                                                                | 23.5 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 64.7 ms                                                                | 62.7 ms: 1.03x faster                                                    |
| nqueens                    | 80.3 ms                                                                | 77.9 ms: 1.03x faster                                                    |
| scimark_fft                | 314 ms                                                                 | 305 ms: 1.03x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 98.9 ms: 1.02x faster                                                    |
| chaos                      | 58.4 ms                                                                | 57.4 ms: 1.02x faster                                                    |
| pickle_pure_python         | 323 us                                                                 | 318 us: 1.02x faster                                                     |
| spectral_norm              | 96.3 ms                                                                | 94.8 ms: 1.02x faster                                                    |
| scimark_lu                 | 110 ms                                                                 | 108 ms: 1.01x faster                                                     |
| dulwich_log                | 76.6 ms                                                                | 75.5 ms: 1.01x faster                                                    |
| thrift                     | 738 us                                                                 | 729 us: 1.01x faster                                                     |
| nbody                      | 90.3 ms                                                                | 89.2 ms: 1.01x faster                                                    |
| django_template            | 35.4 ms                                                                | 35.0 ms: 1.01x faster                                                    |
| subparsers                 | 22.2 ms                                                                | 22.0 ms: 1.01x faster                                                    |
| coverage                   | 79.2 ms                                                                | 78.6 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 2.59 us: 1.01x faster                                                    |
| deepcopy_memo              | 30.1 us                                                                | 30.0 us: 1.01x faster                                                    |
| sympy_integrate            | 19.9 ms                                                                | 19.8 ms: 1.00x faster                                                    |
| 2to3                       | 256 ms                                                                 | 256 ms: 1.00x slower                                                     |
| python_startup_no_site     | 7.49 ms                                                                | 7.52 ms: 1.00x slower                                                    |
| unpickle_pure_python       | 213 us                                                                 | 213 us: 1.00x slower                                                     |
| sqlglot_optimize           | 52.1 ms                                                                | 52.3 ms: 1.00x slower                                                    |
| python_startup             | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                    |
| async_generators           | 352 ms                                                                 | 354 ms: 1.00x slower                                                     |
| tomli_loads                | 1.97 sec                                                               | 1.98 sec: 1.00x slower                                                   |
| bpe_tokeniser              | 4.24 sec                                                               | 4.26 sec: 1.01x slower                                                   |
| connected_components       | 398 ms                                                                 | 400 ms: 1.01x slower                                                     |
| sqlglot_transpile          | 1.57 ms                                                                | 1.58 ms: 1.01x slower                                                    |
| sphinx                     | 992 ms                                                                 | 998 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 90.6 ms                                                                | 91.3 ms: 1.01x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                                    |
| scimark_sor                | 128 ms                                                                 | 129 ms: 1.01x slower                                                     |
| sympy_str                  | 271 ms                                                                 | 273 ms: 1.01x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| deltablue                  | 3.17 ms                                                                | 3.20 ms: 1.01x slower                                                    |
| pyflate                    | 421 ms                                                                 | 425 ms: 1.01x slower                                                     |
| hexiom                     | 5.84 ms                                                                | 5.90 ms: 1.01x slower                                                    |
| sympy_expand               | 453 ms                                                                 | 458 ms: 1.01x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 104 ms: 1.01x slower                                                     |
| richards                   | 44.7 ms                                                                | 45.2 ms: 1.01x slower                                                    |
| telco                      | 7.18 ms                                                                | 7.27 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 610 ms                                                                 | 619 ms: 1.01x slower                                                     |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                    |
| async_tree_none            | 277 ms                                                                 | 281 ms: 1.01x slower                                                     |
| mako                       | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| coroutines                 | 21.6 ms                                                                | 21.9 ms: 1.02x slower                                                    |
| pprint_safe_repr           | 710 ms                                                                 | 721 ms: 1.02x slower                                                     |
| go                         | 117 ms                                                                 | 119 ms: 1.02x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 337 ms: 1.02x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.48 sec: 1.02x slower                                                   |
| richards_super             | 50.7 ms                                                                | 51.5 ms: 1.02x slower                                                    |
| regex_effbot               | 2.69 ms                                                                | 2.74 ms: 1.02x slower                                                    |
| genshi_xml                 | 49.7 ms                                                                | 50.6 ms: 1.02x slower                                                    |
| sqlalchemy_imperative      | 19.1 ms                                                                | 19.4 ms: 1.02x slower                                                    |
| crypto_pyaes               | 65.4 ms                                                                | 66.7 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                                 | 158 us: 1.02x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 130 ms: 1.03x slower                                                     |
| mdp                        | 2.33 sec                                                               | 2.48 sec: 1.06x slower                                                   |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 550 ms: 1.14x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 572 ms: 1.14x slower                                                     |
| pidigits                   | 185 ms                                                                 | 216 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (30): pathlib, xml_etree_process, xml_etree_generate, bench_thread_pool, sympy_sum, docutils, json, generators, raytrace, k_core, asyncio_websockets, deepcopy, xml_etree_parse, fannkuch, async_tree_io, async_tree_memoization_tg, json_loads, comprehensions, many_optionals, shortest_path, async_tree_none_tg, pycparser, sqlite_synth, regex_compile, bench_mp_pool, float, logging_simple, logging_format, pylint, logging_silent

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x