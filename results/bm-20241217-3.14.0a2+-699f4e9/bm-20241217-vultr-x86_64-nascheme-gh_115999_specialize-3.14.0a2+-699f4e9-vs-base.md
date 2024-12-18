# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.005x slower
- HPT reliability: 97.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 352 ms                                                                 | 355 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 258 ms: 1.01x slower                                                     |
| coroutines                 | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 547 ms: 1.13x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 569 ms: 1.14x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_io, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 90.3 ms                                                                | 89.6 ms: 1.01x faster                                                    |
| pidigits       | 185 ms                                                                 | 217 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 165 ms: 1.06x faster                                                     |
| regex_v8       | 24.4 ms                                                                | 23.5 ms: 1.04x faster                                                    |
| regex_effbot   | 2.69 ms                                                                | 2.72 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 323 us                                                                 | 320 us: 1.01x faster                                                     |
| xml_etree_process    | 58.8 ms                                                                | 58.2 ms: 1.01x faster                                                    |
| xml_etree_generate   | 84.5 ms                                                                | 83.8 ms: 1.01x faster                                                    |
| unpickle_pure_python | 213 us                                                                 | 213 us: 1.00x slower                                                     |
| json_loads           | 26.1 us                                                                | 26.2 us: 1.00x slower                                                    |
| xml_etree_iterparse  | 90.6 ms                                                                | 91.2 ms: 1.01x slower                                                    |
| tomli_loads          | 1.97 sec                                                               | 1.98 sec: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.49 ms                                                                | 7.52 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.6 ms                                                                | 11.5 ms: 1.01x faster                                                    |
| django_template | 35.4 ms                                                                | 35.1 ms: 1.01x faster                                                    |
| genshi_xml      | 49.7 ms                                                                | 50.0 ms: 1.01x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna                  | 175 ms                                                                 | 165 ms: 1.06x faster                                                     |
| regex_v8                   | 24.4 ms                                                                | 23.5 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 4.29 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 64.7 ms                                                                | 63.4 ms: 1.02x faster                                                    |
| richards                   | 44.7 ms                                                                | 43.9 ms: 1.02x faster                                                    |
| nqueens                    | 80.3 ms                                                                | 79.0 ms: 1.02x faster                                                    |
| dulwich_log                | 76.6 ms                                                                | 75.5 ms: 1.01x faster                                                    |
| coverage                   | 79.2 ms                                                                | 78.3 ms: 1.01x faster                                                    |
| richards_super             | 50.7 ms                                                                | 50.1 ms: 1.01x faster                                                    |
| pickle_pure_python         | 323 us                                                                 | 320 us: 1.01x faster                                                     |
| xml_etree_process          | 58.8 ms                                                                | 58.2 ms: 1.01x faster                                                    |
| mako                       | 11.6 ms                                                                | 11.5 ms: 1.01x faster                                                    |
| django_template            | 35.4 ms                                                                | 35.1 ms: 1.01x faster                                                    |
| xml_etree_generate         | 84.5 ms                                                                | 83.8 ms: 1.01x faster                                                    |
| generators                 | 27.1 ms                                                                | 26.9 ms: 1.01x faster                                                    |
| subparsers                 | 22.2 ms                                                                | 22.0 ms: 1.01x faster                                                    |
| nbody                      | 90.3 ms                                                                | 89.6 ms: 1.01x faster                                                    |
| thrift                     | 738 us                                                                 | 733 us: 1.01x faster                                                     |
| deepcopy                   | 256 us                                                                 | 254 us: 1.01x faster                                                     |
| deepcopy_memo              | 30.1 us                                                                | 30.0 us: 1.01x faster                                                    |
| pprint_safe_repr           | 710 ms                                                                 | 706 ms: 1.01x faster                                                     |
| sympy_integrate            | 19.9 ms                                                                | 19.8 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 2.59 us: 1.01x faster                                                    |
| mdp                        | 2.33 sec                                                               | 2.32 sec: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                               | 1.12 sec: 1.00x faster                                                   |
| python_startup             | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                    |
| python_startup_no_site     | 7.49 ms                                                                | 7.52 ms: 1.00x slower                                                    |
| sqlglot_optimize           | 52.1 ms                                                                | 52.3 ms: 1.00x slower                                                    |
| unpickle_pure_python       | 213 us                                                                 | 213 us: 1.00x slower                                                     |
| sqlglot_normalize          | 103 ms                                                                 | 103 ms: 1.00x slower                                                     |
| json_loads                 | 26.1 us                                                                | 26.2 us: 1.00x slower                                                    |
| genshi_xml                 | 49.7 ms                                                                | 50.0 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 90.6 ms                                                                | 91.2 ms: 1.01x slower                                                    |
| bpe_tokeniser              | 4.24 sec                                                               | 4.27 sec: 1.01x slower                                                   |
| tomli_loads                | 1.97 sec                                                               | 1.98 sec: 1.01x slower                                                   |
| async_generators           | 352 ms                                                                 | 355 ms: 1.01x slower                                                     |
| regex_effbot               | 2.69 ms                                                                | 2.72 ms: 1.01x slower                                                    |
| spectral_norm              | 96.3 ms                                                                | 97.2 ms: 1.01x slower                                                    |
| pyflate                    | 421 ms                                                                 | 425 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 258 ms: 1.01x slower                                                     |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                    |
| crypto_pyaes               | 65.4 ms                                                                | 66.2 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 1.57 ms                                                                | 1.59 ms: 1.01x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 129 ms: 1.02x slower                                                     |
| sqlalchemy_imperative      | 19.1 ms                                                                | 19.4 ms: 1.02x slower                                                    |
| logging_format             | 6.79 us                                                                | 6.92 us: 1.02x slower                                                    |
| go                         | 117 ms                                                                 | 119 ms: 1.02x slower                                                     |
| comprehensions             | 17.2 us                                                                | 17.5 us: 1.02x slower                                                    |
| hexiom                     | 5.84 ms                                                                | 5.95 ms: 1.02x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 1.28 ms: 1.02x slower                                                    |
| coroutines                 | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                    |
| fannkuch                   | 372 ms                                                                 | 381 ms: 1.02x slower                                                     |
| gc_traversal               | 4.27 ms                                                                | 4.42 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 547 ms: 1.13x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 569 ms: 1.14x slower                                                     |
| pidigits                   | 185 ms                                                                 | 217 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (38): logging_simple, bench_mp_pool, k_core, pathlib, bench_thread_pool, sqlite_synth, logging_silent, sphinx, pprint_pformat, sympy_sum, many_optionals, asyncio_websockets, float, raytrace, 2to3, json_dumps, sympy_str, scimark_sor, chaos, deltablue, sympy_expand, regex_compile, async_tree_io, shortest_path, connected_components, xml_etree_parse, scimark_fft, docutils, async_tree_memoization_tg, scimark_lu, typing_runtime_protocols, telco, meteor_contest, json, async_tree_none, pylint, async_tree_memoization, async_tree_io_tg

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 97.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x