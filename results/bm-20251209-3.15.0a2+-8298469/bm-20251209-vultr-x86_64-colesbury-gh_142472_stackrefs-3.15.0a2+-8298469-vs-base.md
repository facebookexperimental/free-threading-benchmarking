# Results vs. base

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: 8298469
- commit date: 2025-12-09
- overall geometric mean: 1.003x slower
- HPT reliability: 99.27%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 247 ms: 1.01x faster                                                     |
| html5lib       | 61.0 ms                                                                | 60.0 ms: 1.02x faster                                                    |
| sphinx         | 964 ms                                                                 | 974 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines     | 23.8 ms                                                                | 24.4 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (10): async_tree_memoization_tg, async_generators, async_tree_memoization, async_tree_io_tg, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 69.9 ms                                                                | 71.2 ms: 1.02x slower                                                    |
| nbody          | 88.3 ms                                                                | 92.4 ms: 1.05x slower                                                    |
| pidigits       | 196 ms                                                                 | 208 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 177 ms: 1.04x faster                                                     |
| regex_v8       | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                    |
| regex_effbot   | 2.87 ms                                                                | 2.86 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.19 sec                                                               | 2.18 sec: 1.01x faster                                                   |
| xml_etree_iterparse  | 84.1 ms                                                                | 84.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 81.8 ms                                                                | 82.4 ms: 1.01x slower                                                    |
| unpickle_pure_python | 211 us                                                                 | 213 us: 1.01x slower                                                     |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| json_dumps           | 9.66 ms                                                                | 9.82 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.30 ms                                                                | 7.31 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.2 ms                                                                | 48.0 ms: 1.03x faster                                                    |
| django_template | 34.4 ms                                                                | 34.0 ms: 1.01x faster                                                    |
| genshi_text     | 20.5 ms                                                                | 20.4 ms: 1.01x faster                                                    |
| mako            | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark               | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna               | 183 ms                                                                 | 177 ms: 1.04x faster                                                     |
| genshi_xml              | 49.2 ms                                                                | 48.0 ms: 1.03x faster                                                    |
| regex_v8                | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                    |
| thrift                  | 777 us                                                                 | 759 us: 1.02x faster                                                     |
| scimark_fft             | 307 ms                                                                 | 302 ms: 1.02x faster                                                     |
| scimark_sor             | 109 ms                                                                 | 107 ms: 1.02x faster                                                     |
| html5lib                | 61.0 ms                                                                | 60.0 ms: 1.02x faster                                                    |
| hexiom                  | 5.77 ms                                                                | 5.68 ms: 1.01x faster                                                    |
| raytrace                | 255 ms                                                                 | 252 ms: 1.01x faster                                                     |
| django_template         | 34.4 ms                                                                | 34.0 ms: 1.01x faster                                                    |
| deltablue               | 3.38 ms                                                                | 3.35 ms: 1.01x faster                                                    |
| sympy_integrate         | 19.0 ms                                                                | 18.8 ms: 1.01x faster                                                    |
| 2to3                    | 249 ms                                                                 | 247 ms: 1.01x faster                                                     |
| telco                   | 158 ms                                                                 | 157 ms: 1.01x faster                                                     |
| genshi_text             | 20.5 ms                                                                | 20.4 ms: 1.01x faster                                                    |
| regex_effbot            | 2.87 ms                                                                | 2.86 ms: 1.01x faster                                                    |
| tomli_loads             | 2.19 sec                                                               | 2.18 sec: 1.01x faster                                                   |
| sqlglot_v2_parse        | 1.21 ms                                                                | 1.20 ms: 1.00x faster                                                    |
| sympy_sum               | 154 ms                                                                 | 154 ms: 1.00x faster                                                     |
| python_startup          | 12.4 ms                                                                | 12.5 ms: 1.00x slower                                                    |
| python_startup_no_site  | 7.30 ms                                                                | 7.31 ms: 1.00x slower                                                    |
| nqueens                 | 80.0 ms                                                                | 80.2 ms: 1.00x slower                                                    |
| bpe_tokeniser           | 4.19 sec                                                               | 4.21 sec: 1.00x slower                                                   |
| pprint_safe_repr        | 698 ms                                                                 | 701 ms: 1.00x slower                                                     |
| go                      | 106 ms                                                                 | 107 ms: 1.00x slower                                                     |
| mdp                     | 1.14 sec                                                               | 1.15 sec: 1.00x slower                                                   |
| crypto_pyaes            | 69.5 ms                                                                | 69.8 ms: 1.00x slower                                                    |
| many_optionals          | 936 us                                                                 | 940 us: 1.00x slower                                                     |
| deepcopy_memo           | 26.8 us                                                                | 26.9 us: 1.01x slower                                                    |
| comprehensions          | 15.9 us                                                                | 16.0 us: 1.01x slower                                                    |
| xml_etree_iterparse     | 84.1 ms                                                                | 84.7 ms: 1.01x slower                                                    |
| richards_super          | 48.5 ms                                                                | 48.8 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult | 4.32 ms                                                                | 4.35 ms: 1.01x slower                                                    |
| xml_etree_generate      | 81.8 ms                                                                | 82.4 ms: 1.01x slower                                                    |
| spectral_norm           | 95.3 ms                                                                | 96.0 ms: 1.01x slower                                                    |
| sqlglot_v2_normalize    | 101 ms                                                                 | 102 ms: 1.01x slower                                                     |
| k_core                  | 1.87 sec                                                               | 1.88 sec: 1.01x slower                                                   |
| gc_traversal            | 4.43 ms                                                                | 4.47 ms: 1.01x slower                                                    |
| richards                | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                                    |
| mako                    | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| sphinx                  | 964 ms                                                                 | 974 ms: 1.01x slower                                                     |
| scimark_monte_carlo     | 63.2 ms                                                                | 63.9 ms: 1.01x slower                                                    |
| sqlglot_v2_optimize     | 50.4 ms                                                                | 50.9 ms: 1.01x slower                                                    |
| unpickle_pure_python    | 211 us                                                                 | 213 us: 1.01x slower                                                     |
| scimark_lu              | 107 ms                                                                 | 109 ms: 1.01x slower                                                     |
| logging_simple          | 5.86 us                                                                | 5.93 us: 1.01x slower                                                    |
| pprint_pformat          | 1.42 sec                                                               | 1.44 sec: 1.01x slower                                                   |
| deepcopy_reduce         | 2.57 us                                                                | 2.60 us: 1.01x slower                                                    |
| xml_etree_parse         | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| deepcopy                | 243 us                                                                 | 246 us: 1.01x slower                                                     |
| coverage                | 81.2 ms                                                                | 82.3 ms: 1.01x slower                                                    |
| generators              | 27.2 ms                                                                | 27.6 ms: 1.01x slower                                                    |
| connected_components    | 386 ms                                                                 | 391 ms: 1.01x slower                                                     |
| pycparser               | 1.08 sec                                                               | 1.10 sec: 1.02x slower                                                   |
| json_dumps              | 9.66 ms                                                                | 9.82 ms: 1.02x slower                                                    |
| float                   | 69.9 ms                                                                | 71.2 ms: 1.02x slower                                                    |
| sympy_expand            | 473 ms                                                                 | 482 ms: 1.02x slower                                                     |
| dulwich_log             | 66.7 ms                                                                | 68.1 ms: 1.02x slower                                                    |
| create_gc_cycles        | 1.89 ms                                                                | 1.93 ms: 1.02x slower                                                    |
| pyflate                 | 408 ms                                                                 | 417 ms: 1.02x slower                                                     |
| coroutines              | 23.8 ms                                                                | 24.4 ms: 1.03x slower                                                    |
| nbody                   | 88.3 ms                                                                | 92.4 ms: 1.05x slower                                                    |
| pidigits                | 196 ms                                                                 | 208 ms: 1.06x slower                                                     |
| bench_mp_pool           | 298 ms                                                                 | 352 ms: 1.18x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (30): regex_compile, bench_thread_pool, async_tree_memoization_tg, sympy_str, pathlib, xml_etree_process, async_generators, docutils, async_tree_memoization, shortest_path, async_tree_io_tg, asyncio_websockets, pylint, meteor_contest, chaos, pickle_pure_python, async_tree_cpu_io_mixed, json_loads, fannkuch, logging_silent, json, sqlite_synth, async_tree_none_tg, sqlglot_v2_transpile, subparsers, typing_runtime_protocols, logging_format, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 99.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x