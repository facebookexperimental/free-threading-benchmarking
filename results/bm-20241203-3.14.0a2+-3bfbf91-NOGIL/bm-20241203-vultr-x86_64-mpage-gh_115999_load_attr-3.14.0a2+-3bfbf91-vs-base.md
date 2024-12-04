# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr
- machine: linux-x86_64
- commit hash: 3bfbf91
- commit date: 2024-12-03
- overall geometric mean: 1.015x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 370 ms                                                                 | 365 ms: 1.01x faster                                                 |
| docutils       | 3.11 sec                                                               | 3.08 sec: 1.01x faster                                               |
| html5lib       | 101 ms                                                                 | 97.5 ms: 1.03x faster                                                |
| sphinx         | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io              | 860 ms                                                                 | 821 ms: 1.05x faster                                                 |
| async_tree_io_tg           | 831 ms                                                                 | 800 ms: 1.04x faster                                                 |
| async_tree_memoization     | 473 ms                                                                 | 458 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 452 ms                                                                 | 438 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 622 ms                                                                 | 604 ms: 1.03x faster                                                 |
| async_tree_none            | 389 ms                                                                 | 378 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 644 ms                                                                 | 626 ms: 1.03x faster                                                 |
| coroutines                 | 25.4 ms                                                                | 24.8 ms: 1.03x faster                                                |
| async_tree_none_tg         | 361 ms                                                                 | 352 ms: 1.03x faster                                                 |
| async_generators           | 457 ms                                                                 | 455 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 137 ms                                                                 | 130 ms: 1.06x faster                                                 |
| float          | 140 ms                                                                 | 139 ms: 1.00x faster                                                 |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 188 ms                                                                 | 183 ms: 1.03x faster                                                 |
| regex_effbot   | 2.89 ms                                                                | 2.86 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 523 us                                                                 | 511 us: 1.02x faster                                                 |
| json_dumps           | 14.1 ms                                                                | 13.9 ms: 1.01x faster                                                |
| xml_etree_process    | 79.2 ms                                                                | 78.4 ms: 1.01x faster                                                |
| unpickle_pure_python | 335 us                                                                 | 333 us: 1.01x faster                                                 |
| xml_etree_generate   | 98.1 ms                                                                | 97.7 ms: 1.00x faster                                                |
| xml_etree_iterparse  | 91.5 ms                                                                | 92.1 ms: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (3): json_loads, xml_etree_parse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.2 ms: 1.02x faster                                                |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 32.3 ms                                                                | 30.4 ms: 1.06x faster                                                |
| genshi_xml      | 65.3 ms                                                                | 63.0 ms: 1.04x faster                                                |
| django_template | 52.4 ms                                                                | 50.6 ms: 1.03x faster                                                |
| mako            | 17.5 ms                                                                | 17.1 ms: 1.03x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| logging_simple             | 11.1 us                                                                | 10.1 us: 1.09x faster                                                |
| logging_format             | 12.2 us                                                                | 11.3 us: 1.08x faster                                                |
| gc_traversal               | 3.53 ms                                                                | 3.28 ms: 1.08x faster                                                |
| genshi_text                | 32.3 ms                                                                | 30.4 ms: 1.06x faster                                                |
| thrift                     | 1.17 ms                                                                | 1.11 ms: 1.06x faster                                                |
| nbody                      | 137 ms                                                                 | 130 ms: 1.06x faster                                                 |
| async_tree_io              | 860 ms                                                                 | 821 ms: 1.05x faster                                                 |
| spectral_norm              | 123 ms                                                                 | 118 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 831 ms                                                                 | 800 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.31 us                                                                | 2.22 us: 1.04x faster                                                |
| subparsers                 | 31.6 ms                                                                | 30.5 ms: 1.04x faster                                                |
| genshi_xml                 | 65.3 ms                                                                | 63.0 ms: 1.04x faster                                                |
| django_template            | 52.4 ms                                                                | 50.6 ms: 1.03x faster                                                |
| pathlib                    | 20.5 ms                                                                | 19.9 ms: 1.03x faster                                                |
| sqlglot_optimize           | 69.7 ms                                                                | 67.4 ms: 1.03x faster                                                |
| deepcopy_reduce            | 3.58 us                                                                | 3.47 us: 1.03x faster                                                |
| async_tree_memoization     | 473 ms                                                                 | 458 ms: 1.03x faster                                                 |
| pylint                     | 383 ms                                                                 | 372 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 452 ms                                                                 | 438 ms: 1.03x faster                                                 |
| html5lib                   | 101 ms                                                                 | 97.5 ms: 1.03x faster                                                |
| async_tree_cpu_io_mixed_tg | 622 ms                                                                 | 604 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.87 ms                                                                | 1.81 ms: 1.03x faster                                                |
| async_tree_none            | 389 ms                                                                 | 378 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 644 ms                                                                 | 626 ms: 1.03x faster                                                 |
| regex_dna                  | 188 ms                                                                 | 183 ms: 1.03x faster                                                 |
| pprint_pformat             | 2.04 sec                                                               | 1.99 sec: 1.03x faster                                               |
| coroutines                 | 25.4 ms                                                                | 24.8 ms: 1.03x faster                                                |
| async_tree_none_tg         | 361 ms                                                                 | 352 ms: 1.03x faster                                                 |
| deepcopy_memo              | 41.0 us                                                                | 39.9 us: 1.03x faster                                                |
| mako                       | 17.5 ms                                                                | 17.1 ms: 1.03x faster                                                |
| pickle_pure_python         | 523 us                                                                 | 511 us: 1.02x faster                                                 |
| pprint_safe_repr           | 983 ms                                                                 | 963 ms: 1.02x faster                                                 |
| many_optionals             | 1.29 ms                                                                | 1.27 ms: 1.02x faster                                                |
| dulwich_log                | 96.4 ms                                                                | 94.6 ms: 1.02x faster                                                |
| python_startup             | 17.5 ms                                                                | 17.2 ms: 1.02x faster                                                |
| sphinx                     | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                               |
| sqlalchemy_declarative     | 204 ms                                                                 | 201 ms: 1.02x faster                                                 |
| nqueens                    | 97.5 ms                                                                | 96.0 ms: 1.02x faster                                                |
| 2to3                       | 370 ms                                                                 | 365 ms: 1.01x faster                                                 |
| deepcopy                   | 329 us                                                                 | 325 us: 1.01x faster                                                 |
| sqlglot_normalize          | 139 ms                                                                 | 137 ms: 1.01x faster                                                 |
| sqlglot_parse              | 2.62 ms                                                                | 2.58 ms: 1.01x faster                                                |
| json_dumps                 | 14.1 ms                                                                | 13.9 ms: 1.01x faster                                                |
| pycparser                  | 1.54 sec                                                               | 1.52 sec: 1.01x faster                                               |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                 |
| crypto_pyaes               | 91.7 ms                                                                | 90.6 ms: 1.01x faster                                                |
| docutils                   | 3.11 sec                                                               | 3.08 sec: 1.01x faster                                               |
| bench_thread_pool          | 3.38 ms                                                                | 3.34 ms: 1.01x faster                                                |
| richards_super             | 87.7 ms                                                                | 86.8 ms: 1.01x faster                                                |
| xml_etree_process          | 79.2 ms                                                                | 78.4 ms: 1.01x faster                                                |
| regex_effbot               | 2.89 ms                                                                | 2.86 ms: 1.01x faster                                                |
| sqlglot_transpile          | 3.00 ms                                                                | 2.98 ms: 1.01x faster                                                |
| fannkuch                   | 496 ms                                                                 | 492 ms: 1.01x faster                                                 |
| connected_components       | 503 ms                                                                 | 500 ms: 1.01x faster                                                 |
| shortest_path              | 556 ms                                                                 | 552 ms: 1.01x faster                                                 |
| sympy_str                  | 480 ms                                                                 | 477 ms: 1.01x faster                                                 |
| async_generators           | 457 ms                                                                 | 455 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 335 us                                                                 | 333 us: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                |
| scimark_fft                | 402 ms                                                                 | 400 ms: 1.00x faster                                                 |
| xml_etree_generate         | 98.1 ms                                                                | 97.7 ms: 1.00x faster                                                |
| float                      | 140 ms                                                                 | 139 ms: 1.00x faster                                                 |
| k_core                     | 2.42 sec                                                               | 2.42 sec: 1.00x faster                                               |
| pidigits                   | 184 ms                                                                 | 184 ms: 1.00x faster                                                 |
| sympy_integrate            | 29.7 ms                                                                | 29.6 ms: 1.00x faster                                                |
| sympy_sum                  | 353 ms                                                                 | 352 ms: 1.00x faster                                                 |
| mdp                        | 2.85 sec                                                               | 2.86 sec: 1.00x slower                                               |
| xml_etree_iterparse        | 91.5 ms                                                                | 92.1 ms: 1.01x slower                                                |
| comprehensions             | 27.5 us                                                                | 27.7 us: 1.01x slower                                                |
| typing_runtime_protocols   | 204 us                                                                 | 206 us: 1.01x slower                                                 |
| scimark_lu                 | 181 ms                                                                 | 184 ms: 1.02x slower                                                 |
| coverage                   | 102 ms                                                                 | 106 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 5.63 ms                                                                | 6.08 ms: 1.08x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (23): sqlalchemy_imperative, regex_compile, scimark_sor, raytrace, json, sympy_expand, telco, json_loads, deltablue, richards, hexiom, go, asyncio_websockets, scimark_monte_carlo, xml_etree_parse, bpe_tokeniser, chaos, pyflate, tomli_loads, logging_silent, generators, meteor_contest, regex_v8

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x