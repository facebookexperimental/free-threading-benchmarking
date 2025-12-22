# Results vs. base

- fork: chris-eibl
- ref: msvc_tail_call_new
- machine: linux-x86_64
- commit hash: da1adaf
- commit date: 2025-12-22
- overall geometric mean: 1.004x slower
- HPT reliability: 86.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| docutils       | 2.57 sec                                                               | 2.56 sec: 1.00x faster                                                     |
| html5lib       | 60.3 ms                                                                | 59.4 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_generators | 337 ms                                                                 | 343 ms: 1.02x slower                                                       |
| Geometric mean   | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (10): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io_tg, async_tree_memoization_tg, coroutines, async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 69.6 ms                                                                | 71.0 ms: 1.02x slower                                                      |
| pidigits       | 194 ms                                                                 | 205 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                               |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.82 ms: 1.01x faster                                                      |
| regex_dna      | 177 ms                                                                 | 177 ms: 1.00x faster                                                       |
| regex_compile  | 123 ms                                                                 | 124 ms: 1.00x slower                                                       |
| regex_v8       | 21.6 ms                                                                | 23.0 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_loads          | 28.3 us                                                                | 27.7 us: 1.02x faster                                                      |
| xml_etree_process   | 57.6 ms                                                                | 57.1 ms: 1.01x faster                                                      |
| tomli_loads         | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                     |
| xml_etree_iterparse | 84.5 ms                                                                | 84.2 ms: 1.00x faster                                                      |
| xml_etree_generate  | 82.0 ms                                                                | 82.2 ms: 1.00x slower                                                      |
| json_dumps          | 9.98 ms                                                                | 10.0 ms: 1.01x slower                                                      |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.29 ms                                                                | 7.23 ms: 1.01x faster                                                      |
| python_startup         | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 12.0 ms                                                                | 11.7 ms: 1.02x faster                                                      |
| genshi_text    | 21.2 ms                                                                | 21.6 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                | bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3+-700e9fa | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_loads               | 28.3 us                                                                | 27.7 us: 1.02x faster                                                      |
| mako                     | 12.0 ms                                                                | 11.7 ms: 1.02x faster                                                      |
| thrift                   | 775 us                                                                 | 762 us: 1.02x faster                                                       |
| pyflate                  | 415 ms                                                                 | 409 ms: 1.02x faster                                                       |
| html5lib                 | 60.3 ms                                                                | 59.4 ms: 1.02x faster                                                      |
| fannkuch                 | 391 ms                                                                 | 385 ms: 1.01x faster                                                       |
| regex_effbot             | 2.86 ms                                                                | 2.82 ms: 1.01x faster                                                      |
| nqueens                  | 79.4 ms                                                                | 78.5 ms: 1.01x faster                                                      |
| go                       | 106 ms                                                                 | 105 ms: 1.01x faster                                                       |
| sqlglot_v2_transpile     | 1.51 ms                                                                | 1.49 ms: 1.01x faster                                                      |
| scimark_sor              | 108 ms                                                                 | 107 ms: 1.01x faster                                                       |
| xml_etree_process        | 57.6 ms                                                                | 57.1 ms: 1.01x faster                                                      |
| python_startup_no_site   | 7.29 ms                                                                | 7.23 ms: 1.01x faster                                                      |
| deepcopy_memo            | 26.1 us                                                                | 25.9 us: 1.01x faster                                                      |
| tomli_loads              | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                     |
| python_startup           | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                      |
| sympy_sum                | 156 ms                                                                 | 155 ms: 1.01x faster                                                       |
| comprehensions           | 16.1 us                                                                | 16.0 us: 1.00x faster                                                      |
| docutils                 | 2.57 sec                                                               | 2.56 sec: 1.00x faster                                                     |
| xml_etree_iterparse      | 84.5 ms                                                                | 84.2 ms: 1.00x faster                                                      |
| shortest_path            | 435 ms                                                                 | 433 ms: 1.00x faster                                                       |
| pprint_pformat           | 1.42 sec                                                               | 1.42 sec: 1.00x faster                                                     |
| telco                    | 159 ms                                                                 | 158 ms: 1.00x faster                                                       |
| regex_dna                | 177 ms                                                                 | 177 ms: 1.00x faster                                                       |
| bpe_tokeniser            | 4.19 sec                                                               | 4.18 sec: 1.00x faster                                                     |
| mdp                      | 1.16 sec                                                               | 1.15 sec: 1.00x faster                                                     |
| meteor_contest           | 101 ms                                                                 | 101 ms: 1.00x slower                                                       |
| xml_etree_generate       | 82.0 ms                                                                | 82.2 ms: 1.00x slower                                                      |
| sqlglot_v2_optimize      | 50.8 ms                                                                | 50.9 ms: 1.00x slower                                                      |
| k_core                   | 1.86 sec                                                               | 1.86 sec: 1.00x slower                                                     |
| raytrace                 | 254 ms                                                                 | 255 ms: 1.00x slower                                                       |
| regex_compile            | 123 ms                                                                 | 124 ms: 1.00x slower                                                       |
| pycparser                | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                     |
| many_optionals           | 938 us                                                                 | 944 us: 1.01x slower                                                       |
| coverage                 | 81.5 ms                                                                | 82.0 ms: 1.01x slower                                                      |
| json_dumps               | 9.98 ms                                                                | 10.0 ms: 1.01x slower                                                      |
| richards                 | 41.8 ms                                                                | 42.1 ms: 1.01x slower                                                      |
| connected_components     | 385 ms                                                                 | 389 ms: 1.01x slower                                                       |
| hexiom                   | 5.67 ms                                                                | 5.72 ms: 1.01x slower                                                      |
| pathlib                  | 17.3 ms                                                                | 17.4 ms: 1.01x slower                                                      |
| crypto_pyaes             | 68.8 ms                                                                | 69.4 ms: 1.01x slower                                                      |
| richards_super           | 47.6 ms                                                                | 48.2 ms: 1.01x slower                                                      |
| sympy_str                | 271 ms                                                                 | 275 ms: 1.01x slower                                                       |
| create_gc_cycles         | 1.88 ms                                                                | 1.91 ms: 1.02x slower                                                      |
| async_generators         | 337 ms                                                                 | 343 ms: 1.02x slower                                                       |
| genshi_text              | 21.2 ms                                                                | 21.6 ms: 1.02x slower                                                      |
| float                    | 69.6 ms                                                                | 71.0 ms: 1.02x slower                                                      |
| typing_runtime_protocols | 154 us                                                                 | 158 us: 1.02x slower                                                       |
| dulwich_log              | 67.5 ms                                                                | 69.0 ms: 1.02x slower                                                      |
| deepcopy                 | 241 us                                                                 | 246 us: 1.02x slower                                                       |
| logging_silent           | 101 ns                                                                 | 104 ns: 1.03x slower                                                       |
| spectral_norm            | 93.7 ms                                                                | 96.7 ms: 1.03x slower                                                      |
| deepcopy_reduce          | 2.55 us                                                                | 2.65 us: 1.04x slower                                                      |
| pidigits                 | 194 ms                                                                 | 205 ms: 1.06x slower                                                       |
| scimark_sparse_mat_mult  | 4.35 ms                                                                | 4.61 ms: 1.06x slower                                                      |
| regex_v8                 | 21.6 ms                                                                | 23.0 ms: 1.07x slower                                                      |
| gc_traversal             | 4.09 ms                                                                | 4.50 ms: 1.10x slower                                                      |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (37): async_tree_cpu_io_mixed_tg, bench_thread_pool, sympy_expand, scimark_lu, json, subparsers, deltablue, sqlglot_v2_normalize, scimark_monte_carlo, async_tree_cpu_io_mixed, chaos, sphinx, pprint_safe_repr, genshi_xml, 2to3, sqlglot_v2_parse, sqlite_synth, generators, logging_simple, unpickle_pure_python, asyncio_websockets, pickle_pure_python, async_tree_io_tg, sympy_integrate, logging_format, scimark_fft, async_tree_memoization_tg, nbody, xml_etree_parse, django_template, pylint, coroutines, async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_none, bench_mp_pool

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 86.18% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x