# Results vs. base

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.008x slower
- HPT reliability: 99.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 257 ms: 1.00x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 511 ms: 1.01x faster                                                        |
| async_tree_memoization     | 323 ms                                                                 | 320 ms: 1.01x faster                                                        |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 492 ms: 1.01x faster                                                        |
| async_generators           | 335 ms                                                                 | 337 ms: 1.01x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                                |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, coroutines, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 106 ms                                                                 | 102 ms: 1.04x faster                                                        |
| float          | 72.8 ms                                                                | 75.0 ms: 1.03x slower                                                       |
| pidigits       | 191 ms                                                                 | 227 ms: 1.19x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 181 ms: 1.00x faster                                                        |
| regex_v8       | 22.1 ms                                                                | 22.4 ms: 1.01x slower                                                       |
| regex_compile  | 127 ms                                                                 | 129 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.2 us                                                                | 27.0 us: 1.04x faster                                                       |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                        |
| xml_etree_process    | 59.4 ms                                                                | 60.1 ms: 1.01x slower                                                       |
| pickle_pure_python   | 316 us                                                                 | 321 us: 1.02x slower                                                        |
| unpickle_pure_python | 219 us                                                                 | 224 us: 1.02x slower                                                        |
| tomli_loads          | 1.95 sec                                                               | 2.02 sec: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (3): xml_etree_generate, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                       |
| genshi_xml      | 51.3 ms                                                                | 50.5 ms: 1.02x faster                                                       |
| genshi_text     | 22.7 ms                                                                | 22.5 ms: 1.01x faster                                                       |
| mako            | 12.0 ms                                                                | 12.3 ms: 1.03x slower                                                       |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                        | 2.49 sec                                                               | 2.32 sec: 1.07x faster                                                      |
| json_loads                 | 28.2 us                                                                | 27.0 us: 1.04x faster                                                       |
| nbody                      | 106 ms                                                                 | 102 ms: 1.04x faster                                                        |
| logging_format             | 6.90 us                                                                | 6.63 us: 1.04x faster                                                       |
| json                       | 4.96 ms                                                                | 4.86 ms: 1.02x faster                                                       |
| nqueens                    | 83.6 ms                                                                | 81.9 ms: 1.02x faster                                                       |
| django_template            | 36.4 ms                                                                | 35.8 ms: 1.02x faster                                                       |
| genshi_xml                 | 51.3 ms                                                                | 50.5 ms: 1.02x faster                                                       |
| sympy_sum                  | 158 ms                                                                 | 156 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 511 ms: 1.01x faster                                                        |
| logging_simple             | 6.15 us                                                                | 6.07 us: 1.01x faster                                                       |
| telco                      | 7.51 ms                                                                | 7.42 ms: 1.01x faster                                                       |
| async_tree_memoization     | 323 ms                                                                 | 320 ms: 1.01x faster                                                        |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                        |
| pathlib                    | 19.6 ms                                                                | 19.4 ms: 1.01x faster                                                       |
| sympy_expand               | 469 ms                                                                 | 465 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 492 ms: 1.01x faster                                                        |
| many_optionals             | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                                       |
| genshi_text                | 22.7 ms                                                                | 22.5 ms: 1.01x faster                                                       |
| sympy_integrate            | 19.8 ms                                                                | 19.6 ms: 1.01x faster                                                       |
| regex_dna                  | 181 ms                                                                 | 181 ms: 1.00x faster                                                        |
| sqlglot_v2_normalize       | 103 ms                                                                 | 103 ms: 1.00x slower                                                        |
| sqlglot_v2_optimize        | 52.3 ms                                                                | 52.5 ms: 1.00x slower                                                       |
| deepcopy_reduce            | 2.69 us                                                                | 2.70 us: 1.00x slower                                                       |
| 2to3                       | 256 ms                                                                 | 257 ms: 1.00x slower                                                        |
| fannkuch                   | 406 ms                                                                 | 408 ms: 1.00x slower                                                        |
| comprehensions             | 17.0 us                                                                | 17.1 us: 1.01x slower                                                       |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                        |
| sqlalchemy_declarative     | 130 ms                                                                 | 131 ms: 1.01x slower                                                        |
| async_generators           | 335 ms                                                                 | 337 ms: 1.01x slower                                                        |
| sqlglot_v2_transpile       | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                                       |
| coverage                   | 79.8 ms                                                                | 80.5 ms: 1.01x slower                                                       |
| deepcopy                   | 261 us                                                                 | 263 us: 1.01x slower                                                        |
| dulwich_log                | 66.5 ms                                                                | 67.1 ms: 1.01x slower                                                       |
| hexiom                     | 6.05 ms                                                                | 6.10 ms: 1.01x slower                                                       |
| scimark_monte_carlo        | 65.9 ms                                                                | 66.5 ms: 1.01x slower                                                       |
| regex_v8                   | 22.1 ms                                                                | 22.4 ms: 1.01x slower                                                       |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.29 ms: 1.01x slower                                                       |
| pyflate                    | 419 ms                                                                 | 424 ms: 1.01x slower                                                        |
| xml_etree_process          | 59.4 ms                                                                | 60.1 ms: 1.01x slower                                                       |
| deepcopy_memo              | 30.2 us                                                                | 30.6 us: 1.01x slower                                                       |
| pickle_pure_python         | 316 us                                                                 | 321 us: 1.02x slower                                                        |
| regex_compile              | 127 ms                                                                 | 129 ms: 1.02x slower                                                        |
| richards_super             | 48.3 ms                                                                | 49.1 ms: 1.02x slower                                                       |
| sqlite_synth               | 2.19 us                                                                | 2.23 us: 1.02x slower                                                       |
| bpe_tokeniser              | 4.35 sec                                                               | 4.44 sec: 1.02x slower                                                      |
| chaos                      | 57.4 ms                                                                | 58.6 ms: 1.02x slower                                                       |
| pprint_safe_repr           | 721 ms                                                                 | 736 ms: 1.02x slower                                                        |
| unpickle_pure_python       | 219 us                                                                 | 224 us: 1.02x slower                                                        |
| deltablue                  | 3.10 ms                                                                | 3.17 ms: 1.02x slower                                                       |
| logging_silent             | 97.8 ns                                                                | 99.9 ns: 1.02x slower                                                       |
| pprint_pformat             | 1.46 sec                                                               | 1.50 sec: 1.02x slower                                                      |
| scimark_lu                 | 114 ms                                                                 | 117 ms: 1.03x slower                                                        |
| mako                       | 12.0 ms                                                                | 12.3 ms: 1.03x slower                                                       |
| float                      | 72.8 ms                                                                | 75.0 ms: 1.03x slower                                                       |
| raytrace                   | 261 ms                                                                 | 269 ms: 1.03x slower                                                        |
| crypto_pyaes               | 70.2 ms                                                                | 72.4 ms: 1.03x slower                                                       |
| tomli_loads                | 1.95 sec                                                               | 2.02 sec: 1.03x slower                                                      |
| go                         | 112 ms                                                                 | 116 ms: 1.03x slower                                                        |
| scimark_sor                | 113 ms                                                                 | 116 ms: 1.03x slower                                                        |
| scimark_fft                | 323 ms                                                                 | 340 ms: 1.05x slower                                                        |
| spectral_norm              | 91.4 ms                                                                | 97.2 ms: 1.06x slower                                                       |
| scimark_sparse_mat_mult    | 4.55 ms                                                                | 4.97 ms: 1.09x slower                                                       |
| gc_traversal               | 4.25 ms                                                                | 4.64 ms: 1.09x slower                                                       |
| pidigits                   | 191 ms                                                                 | 227 ms: 1.19x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (30): thrift, subparsers, async_tree_memoization_tg, pycparser, pylint, sympy_str, async_tree_none_tg, richards, bench_thread_pool, k_core, python_startup, bench_mp_pool, python_startup_no_site, xml_etree_generate, asyncio_websockets, generators, coroutines, sphinx, json_dumps, docutils, meteor_contest, async_tree_io_tg, typing_runtime_protocols, sqlalchemy_imperative, xml_etree_iterparse, create_gc_cycles, shortest_path, async_tree_io, regex_effbot, connected_components

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 99.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x