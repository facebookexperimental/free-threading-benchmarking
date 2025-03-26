# Results vs. base

- fork: colesbury
- ref: gh_131586_lookup_spe
- machine: linux-x86_64
- commit hash: 4c6bf78
- commit date: 2025-03-25
- overall geometric mean: 1.005x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 242 ms                                                                 | 244 ms: 1.01x slower                                                      |
| docutils       | 2.49 sec                                                               | 2.52 sec: 1.01x slower                                                    |
| sphinx         | 952 ms                                                                 | 964 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 470 ms                                                                 | 473 ms: 1.01x slower                                                      |
| async_tree_none_tg         | 240 ms                                                                 | 241 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed_tg | 447 ms                                                                 | 451 ms: 1.01x slower                                                      |
| async_generators           | 310 ms                                                                 | 313 ms: 1.01x slower                                                      |
| async_tree_none            | 256 ms                                                                 | 260 ms: 1.02x slower                                                      |
| async_tree_memoization_tg  | 284 ms                                                                 | 289 ms: 1.02x slower                                                      |
| coroutines                 | 20.1 ms                                                                | 20.5 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_memoization, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 81.9 ms                                                                | 81.2 ms: 1.01x faster                                                     |
| float          | 68.2 ms                                                                | 68.9 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 122 ms                                                                 | 122 ms: 1.01x slower                                                      |
| regex_v8       | 21.0 ms                                                                | 21.8 ms: 1.04x slower                                                     |
| regex_dna      | 171 ms                                                                 | 184 ms: 1.07x slower                                                      |
| regex_effbot   | 2.77 ms                                                                | 2.99 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.79 sec                                                               | 1.76 sec: 1.02x faster                                                    |
| xml_etree_parse      | 148 ms                                                                 | 149 ms: 1.01x slower                                                      |
| xml_etree_iterparse  | 95.6 ms                                                                | 96.2 ms: 1.01x slower                                                     |
| json_loads           | 26.4 us                                                                | 26.6 us: 1.01x slower                                                     |
| json_dumps           | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                     |
| xml_etree_process    | 54.9 ms                                                                | 55.4 ms: 1.01x slower                                                     |
| xml_etree_generate   | 80.2 ms                                                                | 81.3 ms: 1.01x slower                                                     |
| unpickle_pure_python | 201 us                                                                 | 204 us: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 14.9 ms: 1.00x slower                                                     |
| python_startup_no_site | 8.55 ms                                                                | 8.62 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.6 ms                                                                | 11.5 ms: 1.01x faster                                                     |
| django_template | 32.2 ms                                                                | 32.6 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 3.89 ms                                                                | 3.62 ms: 1.07x faster                                                     |
| scimark_fft                | 282 ms                                                                 | 275 ms: 1.02x faster                                                      |
| tomli_loads                | 1.79 sec                                                               | 1.76 sec: 1.02x faster                                                    |
| deltablue                  | 2.89 ms                                                                | 2.84 ms: 1.02x faster                                                     |
| mako                       | 11.6 ms                                                                | 11.5 ms: 1.01x faster                                                     |
| telco                      | 6.89 ms                                                                | 6.82 ms: 1.01x faster                                                     |
| coverage                   | 74.4 ms                                                                | 73.6 ms: 1.01x faster                                                     |
| deepcopy_memo              | 27.3 us                                                                | 27.0 us: 1.01x faster                                                     |
| pycparser                  | 1.09 sec                                                               | 1.08 sec: 1.01x faster                                                    |
| nbody                      | 81.9 ms                                                                | 81.2 ms: 1.01x faster                                                     |
| go                         | 104 ms                                                                 | 104 ms: 1.01x faster                                                      |
| chaos                      | 50.7 ms                                                                | 50.5 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.44 sec: 1.00x faster                                                    |
| nqueens                    | 72.2 ms                                                                | 72.5 ms: 1.00x slower                                                     |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.46 ms: 1.00x slower                                                     |
| scimark_lu                 | 101 ms                                                                 | 101 ms: 1.00x slower                                                      |
| sqlalchemy_declarative     | 125 ms                                                                 | 125 ms: 1.00x slower                                                      |
| python_startup             | 14.8 ms                                                                | 14.9 ms: 1.00x slower                                                     |
| bpe_tokeniser              | 4.10 sec                                                               | 4.12 sec: 1.01x slower                                                    |
| hexiom                     | 5.41 ms                                                                | 5.44 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 470 ms                                                                 | 473 ms: 1.01x slower                                                      |
| pyflate                    | 385 ms                                                                 | 387 ms: 1.01x slower                                                      |
| richards_super             | 44.2 ms                                                                | 44.4 ms: 1.01x slower                                                     |
| xml_etree_parse            | 148 ms                                                                 | 149 ms: 1.01x slower                                                      |
| bench_thread_pool          | 1.00 ms                                                                | 1.01 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 95.6 ms                                                                | 96.2 ms: 1.01x slower                                                     |
| json_loads                 | 26.4 us                                                                | 26.6 us: 1.01x slower                                                     |
| richards                   | 38.1 ms                                                                | 38.3 ms: 1.01x slower                                                     |
| regex_compile              | 122 ms                                                                 | 122 ms: 1.01x slower                                                      |
| meteor_contest             | 103 ms                                                                 | 104 ms: 1.01x slower                                                      |
| python_startup_no_site     | 8.55 ms                                                                | 8.62 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 240 ms                                                                 | 241 ms: 1.01x slower                                                      |
| generators                 | 26.3 ms                                                                | 26.5 ms: 1.01x slower                                                     |
| sympy_expand               | 438 ms                                                                 | 441 ms: 1.01x slower                                                      |
| sqlglot_v2_parse           | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                     |
| json_dumps                 | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                     |
| 2to3                       | 242 ms                                                                 | 244 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed_tg | 447 ms                                                                 | 451 ms: 1.01x slower                                                      |
| async_generators           | 310 ms                                                                 | 313 ms: 1.01x slower                                                      |
| json                       | 4.84 ms                                                                | 4.89 ms: 1.01x slower                                                     |
| raytrace                   | 235 ms                                                                 | 238 ms: 1.01x slower                                                      |
| docutils                   | 2.49 sec                                                               | 2.52 sec: 1.01x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 379 ms: 1.01x slower                                                      |
| sqlglot_v2_normalize       | 96.8 ms                                                                | 97.7 ms: 1.01x slower                                                     |
| xml_etree_process          | 54.9 ms                                                                | 55.4 ms: 1.01x slower                                                     |
| spectral_norm              | 79.8 ms                                                                | 80.6 ms: 1.01x slower                                                     |
| float                      | 68.2 ms                                                                | 68.9 ms: 1.01x slower                                                     |
| subparsers                 | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                     |
| sympy_str                  | 260 ms                                                                 | 263 ms: 1.01x slower                                                      |
| sympy_integrate            | 18.3 ms                                                                | 18.6 ms: 1.01x slower                                                     |
| sqlalchemy_imperative      | 19.0 ms                                                                | 19.2 ms: 1.01x slower                                                     |
| sphinx                     | 952 ms                                                                 | 964 ms: 1.01x slower                                                      |
| pathlib                    | 18.4 ms                                                                | 18.7 ms: 1.01x slower                                                     |
| xml_etree_generate         | 80.2 ms                                                                | 81.3 ms: 1.01x slower                                                     |
| django_template            | 32.2 ms                                                                | 32.6 ms: 1.01x slower                                                     |
| unpickle_pure_python       | 201 us                                                                 | 204 us: 1.02x slower                                                      |
| async_tree_none            | 256 ms                                                                 | 260 ms: 1.02x slower                                                      |
| dulwich_log                | 64.6 ms                                                                | 65.6 ms: 1.02x slower                                                     |
| async_tree_memoization_tg  | 284 ms                                                                 | 289 ms: 1.02x slower                                                      |
| sqlglot_v2_optimize        | 49.1 ms                                                                | 49.9 ms: 1.02x slower                                                     |
| sympy_sum                  | 148 ms                                                                 | 150 ms: 1.02x slower                                                      |
| sqlite_synth               | 2.13 us                                                                | 2.16 us: 1.02x slower                                                     |
| crypto_pyaes               | 66.6 ms                                                                | 67.9 ms: 1.02x slower                                                     |
| mdp                        | 2.40 sec                                                               | 2.45 sec: 1.02x slower                                                    |
| coroutines                 | 20.1 ms                                                                | 20.5 ms: 1.02x slower                                                     |
| deepcopy                   | 228 us                                                                 | 234 us: 1.03x slower                                                      |
| regex_v8                   | 21.0 ms                                                                | 21.8 ms: 1.04x slower                                                     |
| logging_silent             | 81.8 ns                                                                | 86.3 ns: 1.05x slower                                                     |
| regex_dna                  | 171 ms                                                                 | 184 ms: 1.07x slower                                                      |
| regex_effbot               | 2.77 ms                                                                | 2.99 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (25): logging_simple, deepcopy_reduce, genshi_text, pprint_safe_repr, pickle_pure_python, gc_traversal, comprehensions, scimark_monte_carlo, scimark_sor, many_optionals, k_core, asyncio_websockets, pidigits, async_tree_memoization, bench_mp_pool, create_gc_cycles, shortest_path, logging_format, genshi_xml, typing_runtime_protocols, thrift, async_tree_io, connected_components, async_tree_io_tg, pylint

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x