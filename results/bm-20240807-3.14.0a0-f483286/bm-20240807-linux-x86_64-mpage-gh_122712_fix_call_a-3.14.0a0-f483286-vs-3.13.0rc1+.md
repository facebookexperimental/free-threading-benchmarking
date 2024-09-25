# Results vs. 3.13.0rc1+

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.03x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| html5lib       | 98.1 ms                                                 | 91.1 ms: 1.08x faster                                                |
| tornado_http   | 248 ms                                                  | 268 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                   | 1.00x faster                                                         |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|---------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization    | 745 ms                                                  | 643 ms: 1.16x faster                                                 |
| async_tree_none_tg        | 521 ms                                                  | 456 ms: 1.14x faster                                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.29 sec: 1.13x faster                                               |
| async_tree_none           | 576 ms                                                  | 512 ms: 1.12x faster                                                 |
| async_tree_memoization_tg | 672 ms                                                  | 609 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 819 ms: 1.10x faster                                                 |
| asyncio_tcp               | 985 ms                                                  | 925 ms: 1.07x faster                                                 |
| async_tree_io             | 1.38 sec                                                | 1.30 sec: 1.06x faster                                               |
| coroutines                | 29.2 ms                                                 | 31.1 ms: 1.07x slower                                                |
| Geometric mean            | (ref)                                                   | 1.07x faster                                                         |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_generators, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 124 ms                                                  | 111 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                   | 1.03x faster                                                         |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 34.2 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                   | 1.02x slower                                                         |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_process    | 86.5 ms                                                 | 76.7 ms: 1.13x faster                                                |
| xml_etree_generate   | 129 ms                                                  | 120 ms: 1.08x faster                                                 |
| xml_etree_parse      | 236 ms                                                  | 222 ms: 1.06x faster                                                 |
| unpickle             | 21.4 us                                                 | 20.4 us: 1.05x faster                                                |
| unpickle_pure_python | 296 us                                                  | 282 us: 1.05x faster                                                 |
| unpickle_list        | 6.67 us                                                 | 7.43 us: 1.11x slower                                                |
| Geometric mean       | (ref)                                                   | 1.02x faster                                                         |

Benchmark hidden because not significant (8): xml_etree_iterparse, pickle_dict, tomli_loads, pickle, pickle_pure_python, json_loads, pickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|---------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy                  | 484 us                                                  | 346 us: 1.40x faster                                                 |
| deepcopy_memo             | 51.7 us                                                 | 40.8 us: 1.27x faster                                                |
| deepcopy_reduce           | 4.27 us                                                 | 3.50 us: 1.22x faster                                                |
| async_tree_memoization    | 745 ms                                                  | 643 ms: 1.16x faster                                                 |
| create_gc_cycles          | 2.46 ms                                                 | 2.14 ms: 1.15x faster                                                |
| async_tree_none_tg        | 521 ms                                                  | 456 ms: 1.14x faster                                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.29 sec: 1.13x faster                                               |
| xml_etree_process         | 86.5 ms                                                 | 76.7 ms: 1.13x faster                                                |
| async_tree_none           | 576 ms                                                  | 512 ms: 1.12x faster                                                 |
| meteor_contest            | 157 ms                                                  | 140 ms: 1.12x faster                                                 |
| nbody                     | 124 ms                                                  | 111 ms: 1.12x faster                                                 |
| async_tree_memoization_tg | 672 ms                                                  | 609 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 819 ms: 1.10x faster                                                 |
| richards                  | 65.8 ms                                                 | 60.2 ms: 1.09x faster                                                |
| scimark_lu                | 154 ms                                                  | 142 ms: 1.09x faster                                                 |
| sqlglot_optimize          | 76.2 ms                                                 | 70.4 ms: 1.08x faster                                                |
| gc_traversal              | 5.91 ms                                                 | 5.46 ms: 1.08x faster                                                |
| xml_etree_generate        | 129 ms                                                  | 120 ms: 1.08x faster                                                 |
| html5lib                  | 98.1 ms                                                 | 91.1 ms: 1.08x faster                                                |
| scimark_sparse_mat_mult   | 6.98 ms                                                 | 6.49 ms: 1.08x faster                                                |
| sqlite_synth              | 4.07 us                                                 | 3.80 us: 1.07x faster                                                |
| logging_simple            | 8.98 us                                                 | 8.40 us: 1.07x faster                                                |
| asyncio_tcp               | 985 ms                                                  | 925 ms: 1.07x faster                                                 |
| xml_etree_parse           | 236 ms                                                  | 222 ms: 1.06x faster                                                 |
| async_tree_io             | 1.38 sec                                                | 1.30 sec: 1.06x faster                                               |
| richards_super            | 76.3 ms                                                 | 71.9 ms: 1.06x faster                                                |
| telco                     | 11.4 ms                                                 | 10.8 ms: 1.06x faster                                                |
| raytrace                  | 350 ms                                                  | 331 ms: 1.06x faster                                                 |
| scimark_sor               | 172 ms                                                  | 163 ms: 1.06x faster                                                 |
| unpickle                  | 21.4 us                                                 | 20.4 us: 1.05x faster                                                |
| unpickle_pure_python      | 296 us                                                  | 282 us: 1.05x faster                                                 |
| mdp                       | 3.80 sec                                                | 3.62 sec: 1.05x faster                                               |
| pprint_pformat            | 2.00 sec                                                | 1.93 sec: 1.03x faster                                               |
| regex_v8                  | 32.4 ms                                                 | 34.2 ms: 1.06x slower                                                |
| coroutines                | 29.2 ms                                                 | 31.1 ms: 1.07x slower                                                |
| json                      | 6.55 ms                                                 | 7.01 ms: 1.07x slower                                                |
| tornado_http              | 248 ms                                                  | 268 ms: 1.08x slower                                                 |
| crypto_pyaes              | 99.8 ms                                                 | 108 ms: 1.08x slower                                                 |
| unpickle_list             | 6.67 us                                                 | 7.43 us: 1.11x slower                                                |
| bench_mp_pool             | 19.4 ms                                                 | 22.7 ms: 1.17x slower                                                |
| Geometric mean            | (ref)                                                   | 1.03x faster                                                         |

Benchmark hidden because not significant (56): xml_etree_iterparse, spectral_norm, sqlglot_parse, django_template, sqlglot_transpile, pickle_dict, async_tree_cpu_io_mixed_tg, fannkuch, tomli_loads, sympy_expand, pathlib, asyncio_websockets, python_startup, regex_dna, chaos, docutils, logging_silent, sqlglot_normalize, pidigits, pylint, async_generators, scimark_monte_carlo, 2to3, genshi_xml, sympy_str, go, logging_format, deltablue, asyncio_tcp_ssl, mako, nqueens, bpe_tokeniser, regex_compile, coverage, typing_runtime_protocols, pycparser, pickle, pickle_pure_python, scimark_fft, hexiom, pprint_safe_repr, thrift, pyflate, sympy_integrate, python_startup_no_site, json_loads, genshi_text, float, pickle_list, generators, regex_effbot, unpack_sequence, comprehensions, sympy_sum, json_dumps, bench_thread_pool
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x