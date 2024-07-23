# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.02x faster
- HPT reliability: 99.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 606 ms                                                                | 661 ms: 1.09x slower                                  |
| docutils       | 4.79 sec                                                              | 4.69 sec: 1.02x faster                                |
| html5lib       | 152 ms                                                                | 135 ms: 1.12x faster                                  |
| tornado_http   | 302 ms                                                                | 320 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                                 | 1.00x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io  | 1.29 sec                                                              | 1.25 sec: 1.04x faster                                |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, nbody, pidigits

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_effbot, regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict         | 46.2 us                                                               | 40.4 us: 1.14x faster                                 |
| pickle              | 16.0 us                                                               | 14.4 us: 1.12x faster                                 |
| pickle_list         | 6.94 us                                                               | 6.56 us: 1.06x faster                                 |
| xml_etree_process   | 123 ms                                                                | 119 ms: 1.04x faster                                  |
| xml_etree_iterparse | 156 ms                                                                | 152 ms: 1.03x faster                                  |
| Geometric mean      | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (9): unpickle_list, unpickle, json_dumps, json_loads, unpickle_pure_python, tomli_loads, pickle_pure_python, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 19.7 ms                                                               | 18.6 ms: 1.06x faster                                 |
| python_startup         | 28.8 ms                                                               | 27.3 ms: 1.06x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.06x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 58.5 ms                                                               | 54.8 ms: 1.07x faster                                 |
| mako           | 31.2 ms                                                               | 29.7 ms: 1.05x faster                                 |
| genshi_xml     | 122 ms                                                                | 117 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240722-linux-x86_64-python-2762c6cc5e4c1c0d6305-3.14.0a0-2762c6c | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pathlib                  | 37.5 ms                                                               | 31.7 ms: 1.18x faster                                 |
| pickle_dict              | 46.2 us                                                               | 40.4 us: 1.14x faster                                 |
| html5lib                 | 152 ms                                                                | 135 ms: 1.12x faster                                  |
| pickle                   | 16.0 us                                                               | 14.4 us: 1.12x faster                                 |
| hexiom                   | 18.0 ms                                                               | 16.5 ms: 1.09x faster                                 |
| json                     | 8.72 ms                                                               | 8.04 ms: 1.08x faster                                 |
| sqlglot_optimize         | 131 ms                                                                | 121 ms: 1.08x faster                                  |
| logging_silent           | 260 ns                                                                | 240 ns: 1.08x faster                                  |
| dulwich_log              | 146 ms                                                                | 135 ms: 1.08x faster                                  |
| richards                 | 107 ms                                                                | 99.0 ms: 1.08x faster                                 |
| sqlglot_transpile        | 4.65 ms                                                               | 4.33 ms: 1.07x faster                                 |
| nqueens                  | 163 ms                                                                | 153 ms: 1.07x faster                                  |
| genshi_text              | 58.5 ms                                                               | 54.8 ms: 1.07x faster                                 |
| chaos                    | 175 ms                                                                | 165 ms: 1.06x faster                                  |
| generators               | 56.0 ms                                                               | 52.7 ms: 1.06x faster                                 |
| python_startup_no_site   | 19.7 ms                                                               | 18.6 ms: 1.06x faster                                 |
| python_startup           | 28.8 ms                                                               | 27.3 ms: 1.06x faster                                 |
| pickle_list              | 6.94 us                                                               | 6.56 us: 1.06x faster                                 |
| logging_format           | 17.8 us                                                               | 16.8 us: 1.06x faster                                 |
| meteor_contest           | 206 ms                                                                | 196 ms: 1.05x faster                                  |
| mako                     | 31.2 ms                                                               | 29.7 ms: 1.05x faster                                 |
| richards_super           | 129 ms                                                                | 122 ms: 1.05x faster                                  |
| genshi_xml               | 122 ms                                                                | 117 ms: 1.05x faster                                  |
| unpack_sequence          | 199 ns                                                                | 191 ns: 1.04x faster                                  |
| asyncio_websockets       | 744 ms                                                                | 714 ms: 1.04x faster                                  |
| deltablue                | 11.3 ms                                                               | 10.8 ms: 1.04x faster                                 |
| xml_etree_process        | 123 ms                                                                | 119 ms: 1.04x faster                                  |
| async_tree_io            | 1.29 sec                                                              | 1.25 sec: 1.04x faster                                |
| pycparser                | 2.22 sec                                                              | 2.15 sec: 1.03x faster                                |
| xml_etree_iterparse      | 156 ms                                                                | 152 ms: 1.03x faster                                  |
| docutils                 | 4.79 sec                                                              | 4.69 sec: 1.02x faster                                |
| scimark_fft              | 602 ms                                                                | 616 ms: 1.02x slower                                  |
| async_generators         | 722 ms                                                                | 739 ms: 1.02x slower                                  |
| typing_runtime_protocols | 327 us                                                                | 337 us: 1.03x slower                                  |
| coverage                 | 143 ms                                                                | 149 ms: 1.04x slower                                  |
| mdp                      | 4.85 sec                                                              | 5.07 sec: 1.05x slower                                |
| deepcopy                 | 577 us                                                                | 608 us: 1.05x slower                                  |
| tornado_http             | 302 ms                                                                | 320 ms: 1.06x slower                                  |
| scimark_lu               | 304 ms                                                                | 326 ms: 1.07x slower                                  |
| scimark_sparse_mat_mult  | 8.28 ms                                                               | 9.03 ms: 1.09x slower                                 |
| 2to3                     | 606 ms                                                                | 661 ms: 1.09x slower                                  |
| comprehensions           | 38.3 us                                                               | 42.1 us: 1.10x slower                                 |
| Geometric mean           | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (55): gc_traversal, async_tree_memoization_tg, pylint, sqlglot_normalize, create_gc_cycles, unpickle_list, scimark_monte_carlo, logging_simple, async_tree_cpu_io_mixed_tg, coroutines, go, async_tree_io_tg, sqlglot_parse, unpickle, json_dumps, async_tree_cpu_io_mixed, asyncio_tcp, json_loads, deepcopy_memo, unpickle_pure_python, async_tree_none_tg, regex_effbot, float, sympy_str, sqlite_synth, async_tree_memoization, asyncio_tcp_ssl, regex_compile, raytrace, scimark_sor, nbody, regex_dna, django_template, pprint_pformat, sympy_expand, tomli_loads, sympy_integrate, pidigits, telco, pickle_pure_python, xml_etree_parse, sympy_sum, thrift, bpe_tokeniser, xml_etree_generate, spectral_norm, pyflate, regex_v8, crypto_pyaes, pprint_safe_repr, async_tree_none, deepcopy_reduce, fannkuch, bench_thread_pool, bench_mp_pool

# HPT report

- Reliability score: 99.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x