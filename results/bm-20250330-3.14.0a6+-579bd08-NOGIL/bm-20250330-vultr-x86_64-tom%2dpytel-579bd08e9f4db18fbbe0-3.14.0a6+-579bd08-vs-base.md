# Results vs. base

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.003x slower
- HPT reliability: 52.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| html5lib       | 69.2 ms                                                                | 71.3 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators           | 390 ms                                                                 | 386 ms: 1.01x faster                                                        |
| async_tree_memoization_tg  | 301 ms                                                                 | 299 ms: 1.01x faster                                                        |
| async_tree_io              | 586 ms                                                                 | 583 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed    | 518 ms                                                                 | 523 ms: 1.01x slower                                                        |
| coroutines                 | 23.5 ms                                                                | 23.8 ms: 1.01x slower                                                       |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 491 ms: 1.01x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io_tg, asyncio_websockets, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                       |
| nbody          | 130 ms                                                                 | 135 ms: 1.04x slower                                                        |
| pidigits       | 193 ms                                                                 | 223 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.77 ms: 1.00x faster                                                       |
| regex_dna      | 169 ms                                                                 | 182 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 29.9 us                                                                | 28.8 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 89.0 ms                                                                | 88.1 ms: 1.01x faster                                                       |
| tomli_loads          | 2.38 sec                                                               | 2.36 sec: 1.01x faster                                                      |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                        |
| xml_etree_generate   | 97.3 ms                                                                | 97.6 ms: 1.00x slower                                                       |
| unpickle_pure_python | 255 us                                                                 | 257 us: 1.01x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (3): json_dumps, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.01x faster                                                       |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                       |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 28.6 ms                                                                | 28.2 ms: 1.01x faster                                                       |
| mako            | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                       |
| genshi_xml      | 59.8 ms                                                                | 59.3 ms: 1.01x faster                                                       |
| django_template | 43.1 ms                                                                | 43.3 ms: 1.00x slower                                                       |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads                 | 29.9 us                                                                | 28.8 us: 1.04x faster                                                       |
| logging_format             | 8.50 us                                                                | 8.22 us: 1.03x faster                                                       |
| deepcopy_reduce            | 3.22 us                                                                | 3.13 us: 1.03x faster                                                       |
| thrift                     | 888 us                                                                 | 868 us: 1.02x faster                                                        |
| create_gc_cycles           | 1.38 ms                                                                | 1.35 ms: 1.02x faster                                                       |
| logging_simple             | 7.36 us                                                                | 7.22 us: 1.02x faster                                                       |
| fannkuch                   | 498 ms                                                                 | 490 ms: 1.02x faster                                                        |
| gc_traversal               | 1.82 ms                                                                | 1.79 ms: 1.02x faster                                                       |
| genshi_text                | 28.6 ms                                                                | 28.2 ms: 1.01x faster                                                       |
| telco                      | 9.06 ms                                                                | 8.95 ms: 1.01x faster                                                       |
| deepcopy_memo              | 39.5 us                                                                | 39.1 us: 1.01x faster                                                       |
| mako                       | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                       |
| async_generators           | 390 ms                                                                 | 386 ms: 1.01x faster                                                        |
| richards_super             | 64.4 ms                                                                | 63.8 ms: 1.01x faster                                                       |
| xml_etree_iterparse        | 89.0 ms                                                                | 88.1 ms: 1.01x faster                                                       |
| tomli_loads                | 2.38 sec                                                               | 2.36 sec: 1.01x faster                                                      |
| spectral_norm              | 115 ms                                                                 | 114 ms: 1.01x faster                                                        |
| sqlalchemy_declarative     | 159 ms                                                                 | 157 ms: 1.01x faster                                                        |
| sympy_str                  | 337 ms                                                                 | 334 ms: 1.01x faster                                                        |
| genshi_xml                 | 59.8 ms                                                                | 59.3 ms: 1.01x faster                                                       |
| sqlglot_v2_normalize       | 121 ms                                                                 | 120 ms: 1.01x faster                                                        |
| richards                   | 55.2 ms                                                                | 54.8 ms: 1.01x faster                                                       |
| json                       | 5.06 ms                                                                | 5.02 ms: 1.01x faster                                                       |
| dulwich_log                | 73.3 ms                                                                | 72.8 ms: 1.01x faster                                                       |
| sqlglot_v2_optimize        | 61.4 ms                                                                | 61.0 ms: 1.01x faster                                                       |
| async_tree_memoization_tg  | 301 ms                                                                 | 299 ms: 1.01x faster                                                        |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                        |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.01x faster                                                       |
| async_tree_io              | 586 ms                                                                 | 583 ms: 1.01x faster                                                        |
| sympy_sum                  | 186 ms                                                                 | 185 ms: 1.00x faster                                                        |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                       |
| regex_effbot               | 2.78 ms                                                                | 2.77 ms: 1.00x faster                                                       |
| coverage                   | 108 ms                                                                 | 109 ms: 1.00x slower                                                        |
| xml_etree_generate         | 97.3 ms                                                                | 97.6 ms: 1.00x slower                                                       |
| django_template            | 43.1 ms                                                                | 43.3 ms: 1.00x slower                                                       |
| pyflate                    | 498 ms                                                                 | 501 ms: 1.01x slower                                                        |
| bpe_tokeniser              | 4.84 sec                                                               | 4.87 sec: 1.01x slower                                                      |
| chaos                      | 68.0 ms                                                                | 68.6 ms: 1.01x slower                                                       |
| deltablue                  | 3.87 ms                                                                | 3.91 ms: 1.01x slower                                                       |
| async_tree_cpu_io_mixed    | 518 ms                                                                 | 523 ms: 1.01x slower                                                        |
| unpickle_pure_python       | 255 us                                                                 | 257 us: 1.01x slower                                                        |
| coroutines                 | 23.5 ms                                                                | 23.8 ms: 1.01x slower                                                       |
| float                      | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                       |
| scimark_lu                 | 142 ms                                                                 | 144 ms: 1.01x slower                                                        |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 491 ms: 1.01x slower                                                        |
| logging_silent             | 114 ns                                                                 | 116 ns: 1.01x slower                                                        |
| scimark_fft                | 394 ms                                                                 | 399 ms: 1.01x slower                                                        |
| scimark_sor                | 135 ms                                                                 | 137 ms: 1.02x slower                                                        |
| raytrace                   | 321 ms                                                                 | 326 ms: 1.02x slower                                                        |
| pprint_pformat             | 1.72 sec                                                               | 1.75 sec: 1.02x slower                                                      |
| scimark_monte_carlo        | 82.8 ms                                                                | 84.5 ms: 1.02x slower                                                       |
| crypto_pyaes               | 88.0 ms                                                                | 90.0 ms: 1.02x slower                                                       |
| generators                 | 31.2 ms                                                                | 32.0 ms: 1.03x slower                                                       |
| pprint_safe_repr           | 827 ms                                                                 | 851 ms: 1.03x slower                                                        |
| html5lib                   | 69.2 ms                                                                | 71.3 ms: 1.03x slower                                                       |
| hexiom                     | 7.49 ms                                                                | 7.75 ms: 1.03x slower                                                       |
| scimark_sparse_mat_mult    | 5.49 ms                                                                | 5.71 ms: 1.04x slower                                                       |
| mdp                        | 2.67 sec                                                               | 2.79 sec: 1.04x slower                                                      |
| nbody                      | 130 ms                                                                 | 135 ms: 1.04x slower                                                        |
| regex_dna                  | 169 ms                                                                 | 182 ms: 1.08x slower                                                        |
| pidigits                   | 193 ms                                                                 | 223 ms: 1.15x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (35): sqlalchemy_imperative, pylint, docutils, typing_runtime_protocols, connected_components, json_dumps, async_tree_none_tg, shortest_path, sympy_expand, bench_mp_pool, meteor_contest, sympy_integrate, deepcopy, pathlib, async_tree_io_tg, many_optionals, comprehensions, sqlglot_v2_parse, pycparser, 2to3, regex_compile, asyncio_websockets, bench_thread_pool, sqlite_synth, xml_etree_process, k_core, subparsers, sphinx, nqueens, pickle_pure_python, go, async_tree_memoization, sqlglot_v2_transpile, async_tree_none, regex_v8

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 52.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x