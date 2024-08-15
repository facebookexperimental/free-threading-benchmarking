# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.01x slower
- HPT reliability: 82.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 5.35 sec                                                              | 5.02 sec: 1.07x faster                                |
| tornado_http   | 350 ms                                                                | 429 ms: 1.23x slower                                  |
| Geometric mean | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg | 672 ms                                                                | 647 ms: 1.04x faster                                  |
| async_tree_io_tg          | 1.14 sec                                                              | 1.19 sec: 1.04x slower                                |
| async_tree_none_tg        | 490 ms                                                                | 510 ms: 1.04x slower                                  |
| async_generators          | 731 ms                                                                | 763 ms: 1.04x slower                                  |
| async_tree_io             | 1.28 sec                                                              | 1.34 sec: 1.05x slower                                |
| async_tree_cpu_io_mixed   | 926 ms                                                                | 974 ms: 1.05x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (7): asyncio_tcp, async_tree_memoization, async_tree_none, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 251 ms                                                                | 275 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_effbot, regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps         | 19.0 ms                                                               | 17.9 ms: 1.06x faster                                 |
| tomli_loads        | 4.23 sec                                                              | 4.36 sec: 1.03x slower                                |
| xml_etree_generate | 167 ms                                                                | 180 ms: 1.08x slower                                  |
| json_loads         | 44.8 us                                                               | 48.4 us: 1.08x slower                                 |
| pickle_dict        | 42.2 us                                                               | 46.3 us: 1.10x slower                                 |
| pickle             | 13.8 us                                                               | 15.8 us: 1.14x slower                                 |
| pickle_pure_python | 783 us                                                                | 910 us: 1.16x slower                                  |
| Geometric mean     | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (7): unpickle, unpickle_pure_python, pickle_list, xml_etree_iterparse, unpickle_list, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 20.9 ms                                                               | 22.7 ms: 1.09x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 87.7 ms                                                               | 80.8 ms: 1.09x faster                                 |
| genshi_text     | 55.2 ms                                                               | 59.2 ms: 1.07x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy_reduce           | 6.61 us                                                               | 5.58 us: 1.18x faster                                 |
| bench_thread_pool         | 5.33 ms                                                               | 4.67 ms: 1.14x faster                                 |
| unpack_sequence           | 212 ns                                                                | 191 ns: 1.11x faster                                  |
| generators                | 58.2 ms                                                               | 53.0 ms: 1.10x faster                                 |
| deepcopy_memo             | 77.4 us                                                               | 70.9 us: 1.09x faster                                 |
| django_template           | 87.7 ms                                                               | 80.8 ms: 1.09x faster                                 |
| crypto_pyaes              | 161 ms                                                                | 150 ms: 1.08x faster                                  |
| docutils                  | 5.35 sec                                                              | 5.02 sec: 1.07x faster                                |
| json_dumps                | 19.0 ms                                                               | 17.9 ms: 1.06x faster                                 |
| deltablue                 | 11.8 ms                                                               | 11.3 ms: 1.05x faster                                 |
| hexiom                    | 16.9 ms                                                               | 16.3 ms: 1.04x faster                                 |
| async_tree_memoization_tg | 672 ms                                                                | 647 ms: 1.04x faster                                  |
| fannkuch                  | 814 ms                                                                | 786 ms: 1.04x faster                                  |
| bpe_tokeniser             | 10.7 sec                                                              | 10.3 sec: 1.03x faster                                |
| tomli_loads               | 4.23 sec                                                              | 4.36 sec: 1.03x slower                                |
| raytrace                  | 789 ms                                                                | 816 ms: 1.03x slower                                  |
| async_tree_io_tg          | 1.14 sec                                                              | 1.19 sec: 1.04x slower                                |
| async_tree_none_tg        | 490 ms                                                                | 510 ms: 1.04x slower                                  |
| sympy_expand              | 1.26 sec                                                              | 1.31 sec: 1.04x slower                                |
| async_generators          | 731 ms                                                                | 763 ms: 1.04x slower                                  |
| sympy_str                 | 697 ms                                                                | 730 ms: 1.05x slower                                  |
| async_tree_io             | 1.28 sec                                                              | 1.34 sec: 1.05x slower                                |
| async_tree_cpu_io_mixed   | 926 ms                                                                | 974 ms: 1.05x slower                                  |
| scimark_monte_carlo       | 161 ms                                                                | 170 ms: 1.06x slower                                  |
| sympy_integrate           | 45.4 ms                                                               | 48.4 ms: 1.07x slower                                 |
| nqueens                   | 164 ms                                                                | 175 ms: 1.07x slower                                  |
| genshi_text               | 55.2 ms                                                               | 59.2 ms: 1.07x slower                                 |
| xml_etree_generate        | 167 ms                                                                | 180 ms: 1.08x slower                                  |
| json_loads                | 44.8 us                                                               | 48.4 us: 1.08x slower                                 |
| python_startup_no_site    | 20.9 ms                                                               | 22.7 ms: 1.09x slower                                 |
| pidigits                  | 251 ms                                                                | 275 ms: 1.10x slower                                  |
| pickle_dict               | 42.2 us                                                               | 46.3 us: 1.10x slower                                 |
| sympy_sum                 | 462 ms                                                                | 509 ms: 1.10x slower                                  |
| pickle                    | 13.8 us                                                               | 15.8 us: 1.14x slower                                 |
| pickle_pure_python        | 783 us                                                                | 910 us: 1.16x slower                                  |
| tornado_http              | 350 ms                                                                | 429 ms: 1.23x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (60): bench_mp_pool, genshi_xml, deepcopy, regex_effbot, coverage, scimark_sparse_mat_mult, pylint, mako, asyncio_tcp, sqlglot_transpile, float, scimark_fft, regex_compile, async_tree_memoization, async_tree_none, asyncio_tcp_ssl, pprint_safe_repr, pprint_pformat, unpickle, chaos, spectral_norm, regex_dna, unpickle_pure_python, pycparser, regex_v8, scimark_sor, logging_silent, logging_simple, pickle_list, meteor_contest, xml_etree_iterparse, pathlib, richards, comprehensions, mdp, unpickle_list, sqlglot_parse, python_startup, pyflate, async_tree_cpu_io_mixed_tg, html5lib, sqlite_synth, coroutines, 2to3, asyncio_websockets, thrift, json, xml_etree_process, sqlglot_normalize, gc_traversal, richards_super, go, xml_etree_parse, telco, nbody, scimark_lu, logging_format, typing_runtime_protocols, create_gc_cycles, sqlglot_optimize

# HPT report

- Reliability score: 82.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x