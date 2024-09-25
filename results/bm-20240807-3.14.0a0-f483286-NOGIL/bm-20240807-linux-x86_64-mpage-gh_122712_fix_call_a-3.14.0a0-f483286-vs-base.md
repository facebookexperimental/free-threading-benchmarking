# Results vs. base

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.00x slower
- HPT reliability: 76.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 694 ms                                                                | 646 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                         |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 883 ms                                                                | 824 ms: 1.07x faster                                                 |
| async_tree_none            | 627 ms                                                                | 585 ms: 1.07x faster                                                 |
| async_tree_io              | 1.33 sec                                                              | 1.25 sec: 1.06x faster                                               |
| async_tree_cpu_io_mixed    | 981 ms                                                                | 933 ms: 1.05x faster                                                 |
| async_tree_none_tg         | 515 ms                                                                | 491 ms: 1.05x faster                                                 |
| asyncio_websockets         | 786 ms                                                                | 753 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 1.19 sec                                                              | 1.15 sec: 1.04x faster                                               |
| asyncio_tcp_ssl            | 3.49 sec                                                              | 3.36 sec: 1.04x faster                                               |
| Geometric mean             | (ref)                                                                 | 1.03x faster                                                         |

Benchmark hidden because not significant (5): asyncio_tcp, coroutines, async_tree_memoization, async_tree_memoization_tg, async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.57 ms                                                               | 4.82 ms: 1.06x slower                                                |
| regex_v8       | 34.7 ms                                                               | 39.2 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                         |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|--------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps         | 18.5 ms                                                               | 17.7 ms: 1.05x faster                                                |
| pickle_list        | 6.51 us                                                               | 6.91 us: 1.06x slower                                                |
| xml_etree_generate | 153 ms                                                                | 164 ms: 1.07x slower                                                 |
| json_loads         | 41.5 us                                                               | 45.4 us: 1.09x slower                                                |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                                         |

Benchmark hidden because not significant (10): unpickle, tomli_loads, pickle, unpickle_list, pickle_dict, pickle_pure_python, unpickle_pure_python, xml_etree_iterparse, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 19.6 ms                                                               | 20.7 ms: 1.06x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.03x slower                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 86.9 ms                                                               | 77.1 ms: 1.13x faster                                                |
| genshi_xml      | 129 ms                                                                | 118 ms: 1.10x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                                         |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template            | 86.9 ms                                                               | 77.1 ms: 1.13x faster                                                |
| genshi_xml                 | 129 ms                                                                | 118 ms: 1.10x faster                                                 |
| deepcopy_reduce            | 6.34 us                                                               | 5.84 us: 1.09x faster                                                |
| scimark_monte_carlo        | 173 ms                                                                | 160 ms: 1.08x faster                                                 |
| 2to3                       | 694 ms                                                                | 646 ms: 1.08x faster                                                 |
| deepcopy_memo              | 74.7 us                                                               | 69.7 us: 1.07x faster                                                |
| async_tree_cpu_io_mixed_tg | 883 ms                                                                | 824 ms: 1.07x faster                                                 |
| async_tree_none            | 627 ms                                                                | 585 ms: 1.07x faster                                                 |
| richards_super             | 133 ms                                                                | 124 ms: 1.07x faster                                                 |
| deepcopy                   | 594 us                                                                | 556 us: 1.07x faster                                                 |
| async_tree_io              | 1.33 sec                                                              | 1.25 sec: 1.06x faster                                               |
| async_tree_cpu_io_mixed    | 981 ms                                                                | 933 ms: 1.05x faster                                                 |
| async_tree_none_tg         | 515 ms                                                                | 491 ms: 1.05x faster                                                 |
| json_dumps                 | 18.5 ms                                                               | 17.7 ms: 1.05x faster                                                |
| asyncio_websockets         | 786 ms                                                                | 753 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 1.19 sec                                                              | 1.15 sec: 1.04x faster                                               |
| asyncio_tcp_ssl            | 3.49 sec                                                              | 3.36 sec: 1.04x faster                                               |
| fannkuch                   | 801 ms                                                                | 776 ms: 1.03x faster                                                 |
| pycparser                  | 2.18 sec                                                              | 2.29 sec: 1.05x slower                                               |
| nqueens                    | 153 ms                                                                | 161 ms: 1.05x slower                                                 |
| richards                   | 105 ms                                                                | 110 ms: 1.05x slower                                                 |
| regex_effbot               | 4.57 ms                                                               | 4.82 ms: 1.06x slower                                                |
| python_startup_no_site     | 19.6 ms                                                               | 20.7 ms: 1.06x slower                                                |
| go                         | 422 ms                                                                | 446 ms: 1.06x slower                                                 |
| thrift                     | 1.67 ms                                                               | 1.77 ms: 1.06x slower                                                |
| pickle_list                | 6.51 us                                                               | 6.91 us: 1.06x slower                                                |
| xml_etree_generate         | 153 ms                                                                | 164 ms: 1.07x slower                                                 |
| json_loads                 | 41.5 us                                                               | 45.4 us: 1.09x slower                                                |
| regex_v8                   | 34.7 ms                                                               | 39.2 ms: 1.13x slower                                                |
| sqlglot_parse              | 3.68 ms                                                               | 4.43 ms: 1.20x slower                                                |
| sqlglot_optimize           | 119 ms                                                                | 143 ms: 1.21x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                         |

Benchmark hidden because not significant (65): unpickle, asyncio_tcp, coroutines, scimark_sparse_mat_mult, html5lib, deltablue, meteor_contest, scimark_sor, telco, regex_compile, pprint_safe_repr, bench_thread_pool, chaos, pidigits, nbody, tornado_http, crypto_pyaes, logging_silent, mdp, bpe_tokeniser, json, pylint, raytrace, logging_simple, comprehensions, sympy_str, python_startup, sympy_expand, tomli_loads, unpack_sequence, mako, pickle, pprint_pformat, coverage, regex_dna, typing_runtime_protocols, async_tree_memoization, sympy_integrate, unpickle_list, pickle_dict, async_tree_memoization_tg, pathlib, scimark_lu, pickle_pure_python, pyflate, sympy_sum, genshi_text, scimark_fft, docutils, unpickle_pure_python, sqlglot_normalize, gc_traversal, async_generators, sqlglot_transpile, spectral_norm, bench_mp_pool, generators, hexiom, xml_etree_iterparse, float, sqlite_synth, xml_etree_process, xml_etree_parse, logging_format, create_gc_cycles

# HPT report

- Reliability score: 76.87% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x