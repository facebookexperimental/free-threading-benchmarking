# Results vs. base

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.00x faster
- HPT reliability: 98.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| tornado_http   | 220 ms                                                                | 268 ms: 1.22x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                         |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp            | 990 ms                                                                | 925 ms: 1.07x faster                                                 |
| async_tree_none        | 547 ms                                                                | 512 ms: 1.07x faster                                                 |
| async_tree_none_tg     | 485 ms                                                                | 456 ms: 1.06x faster                                                 |
| async_tree_memoization | 676 ms                                                                | 643 ms: 1.05x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.03x faster                                                         |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, coroutines, asyncio_websockets, async_tree_io_tg, asyncio_tcp_ssl, async_tree_io, async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 303 ms                                                                | 283 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                         |

Benchmark hidden because not significant (3): regex_v8, regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|---------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_process   | 80.5 ms                                                               | 76.7 ms: 1.05x faster                                                |
| tomli_loads         | 2.65 sec                                                              | 2.74 sec: 1.03x slower                                               |
| unpickle_list       | 7.17 us                                                               | 7.43 us: 1.04x slower                                                |
| pickle_list         | 6.72 us                                                               | 6.99 us: 1.04x slower                                                |
| pickle_pure_python  | 403 us                                                                | 420 us: 1.04x slower                                                 |
| json_dumps          | 14.7 ms                                                               | 15.7 ms: 1.07x slower                                                |
| xml_etree_iterparse | 152 ms                                                                | 165 ms: 1.08x slower                                                 |
| xml_etree_generate  | 111 ms                                                                | 120 ms: 1.08x slower                                                 |
| Geometric mean      | (ref)                                                                 | 1.02x slower                                                         |

Benchmark hidden because not significant (6): xml_etree_parse, json_loads, pickle_dict, pickle, unpickle_pure_python, unpickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 47.1 ms                                                               | 45.2 ms: 1.04x faster                                                |
| genshi_xml      | 64.1 ms                                                               | 68.1 ms: 1.06x slower                                                |
| genshi_text     | 30.4 ms                                                               | 32.3 ms: 1.06x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                         |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark              | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| meteor_contest         | 161 ms                                                                | 140 ms: 1.15x faster                                                 |
| deepcopy               | 378 us                                                                | 346 us: 1.09x faster                                                 |
| asyncio_tcp            | 990 ms                                                                | 925 ms: 1.07x faster                                                 |
| regex_dna              | 303 ms                                                                | 283 ms: 1.07x faster                                                 |
| async_tree_none        | 547 ms                                                                | 512 ms: 1.07x faster                                                 |
| async_tree_none_tg     | 485 ms                                                                | 456 ms: 1.06x faster                                                 |
| pyflate                | 710 ms                                                                | 671 ms: 1.06x faster                                                 |
| create_gc_cycles       | 2.26 ms                                                               | 2.14 ms: 1.06x faster                                                |
| async_tree_memoization | 676 ms                                                                | 643 ms: 1.05x faster                                                 |
| xml_etree_process      | 80.5 ms                                                               | 76.7 ms: 1.05x faster                                                |
| gc_traversal           | 5.71 ms                                                               | 5.46 ms: 1.05x faster                                                |
| django_template        | 47.1 ms                                                               | 45.2 ms: 1.04x faster                                                |
| scimark_lu             | 148 ms                                                                | 142 ms: 1.04x faster                                                 |
| logging_silent         | 134 ns                                                                | 128 ns: 1.04x faster                                                 |
| pycparser              | 1.65 sec                                                              | 1.58 sec: 1.04x faster                                               |
| raytrace               | 343 ms                                                                | 331 ms: 1.04x faster                                                 |
| tomli_loads            | 2.65 sec                                                              | 2.74 sec: 1.03x slower                                               |
| unpickle_list          | 7.17 us                                                               | 7.43 us: 1.04x slower                                                |
| pickle_list            | 6.72 us                                                               | 6.99 us: 1.04x slower                                                |
| pickle_pure_python     | 403 us                                                                | 420 us: 1.04x slower                                                 |
| scimark_fft            | 457 ms                                                                | 480 ms: 1.05x slower                                                 |
| deepcopy_memo          | 38.8 us                                                               | 40.8 us: 1.05x slower                                                |
| genshi_xml             | 64.1 ms                                                               | 68.1 ms: 1.06x slower                                                |
| genshi_text            | 30.4 ms                                                               | 32.3 ms: 1.06x slower                                                |
| crypto_pyaes           | 101 ms                                                                | 108 ms: 1.07x slower                                                 |
| json_dumps             | 14.7 ms                                                               | 15.7 ms: 1.07x slower                                                |
| xml_etree_iterparse    | 152 ms                                                                | 165 ms: 1.08x slower                                                 |
| xml_etree_generate     | 111 ms                                                                | 120 ms: 1.08x slower                                                 |
| go                     | 180 ms                                                                | 195 ms: 1.09x slower                                                 |
| tornado_http           | 220 ms                                                                | 268 ms: 1.22x slower                                                 |
| unpack_sequence        | 56.2 ns                                                               | 76.4 ns: 1.36x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                         |

Benchmark hidden because not significant (65): async_tree_memoization_tg, bench_thread_pool, pylint, xml_etree_parse, mako, typing_runtime_protocols, regex_v8, logging_format, spectral_norm, sqlglot_optimize, html5lib, async_tree_cpu_io_mixed_tg, sqlglot_normalize, deepcopy_reduce, sympy_str, pathlib, json_loads, nbody, chaos, logging_simple, generators, python_startup, scimark_monte_carlo, python_startup_no_site, regex_compile, comprehensions, scimark_sor, sqlite_synth, pickle_dict, richards, async_tree_cpu_io_mixed, coroutines, asyncio_websockets, async_tree_io_tg, hexiom, pickle, docutils, sqlglot_transpile, pidigits, sqlglot_parse, mdp, bpe_tokeniser, 2to3, asyncio_tcp_ssl, async_tree_io, async_generators, pprint_pformat, telco, fannkuch, unpickle_pure_python, deltablue, float, coverage, richards_super, json, nqueens, regex_effbot, pprint_safe_repr, thrift, sympy_integrate, unpickle, bench_mp_pool, sympy_expand, scimark_sparse_mat_mult, sympy_sum

# HPT report

- Reliability score: 98.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x