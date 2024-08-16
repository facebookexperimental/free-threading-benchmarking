# Results vs. 3.12.0b1

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.88x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| docutils       | 4.06 sec                                                              | 3.95 sec: 1.03x faster                                               |
| html5lib       | 95.8 ms                                                               | 91.1 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                         |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 609 ms: 1.53x faster                                                 |
| async_tree_none_tg         | 692 ms                                                                | 456 ms: 1.52x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 643 ms: 1.48x faster                                                 |
| async_tree_none            | 740 ms                                                                | 512 ms: 1.44x faster                                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.29 sec: 1.40x faster                                               |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 819 ms: 1.39x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.38x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 826 ms: 1.33x faster                                                 |
| async_generators           | 617 ms                                                                | 588 ms: 1.05x faster                                                 |
| asyncio_tcp                | 958 ms                                                                | 925 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                                 | 1.25x faster                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 125 ms                                                                | 111 ms: 1.13x faster                                                 |
| float          | 127 ms                                                                | 117 ms: 1.08x faster                                                 |
| pidigits       | 255 ms                                                                | 245 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.08x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 178 ms: 1.11x faster                                                 |
| regex_v8       | 31.1 ms                                                               | 34.2 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                         |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 319 us                                                                | 282 us: 1.13x faster                                                 |
| xml_etree_process    | 85.7 ms                                                               | 76.7 ms: 1.12x faster                                                |
| tomli_loads          | 2.99 sec                                                              | 2.74 sec: 1.09x faster                                               |
| xml_etree_generate   | 128 ms                                                                | 120 ms: 1.07x faster                                                 |
| pickle_pure_python   | 447 us                                                                | 420 us: 1.07x faster                                                 |
| pickle_dict          | 46.5 us                                                               | 45.2 us: 1.03x faster                                                |
| pickle               | 14.8 us                                                               | 15.5 us: 1.04x slower                                                |
| pickle_list          | 6.40 us                                                               | 6.99 us: 1.09x slower                                                |
| json_dumps           | 13.6 ms                                                               | 15.7 ms: 1.16x slower                                                |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                         |

Benchmark hidden because not significant (5): xml_etree_parse, json_loads, unpickle, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 14.9 ms: 1.09x faster                                                |
| Geometric mean         | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 68.1 ms: 1.08x faster                                                |
| django_template | 48.6 ms                                                               | 45.2 ms: 1.07x faster                                                |
| mako            | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                                |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                                         |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 609 ms: 1.53x faster                                                 |
| async_tree_none_tg         | 692 ms                                                                | 456 ms: 1.52x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 643 ms: 1.48x faster                                                 |
| deepcopy                   | 503 us                                                                | 346 us: 1.45x faster                                                 |
| async_tree_none            | 740 ms                                                                | 512 ms: 1.44x faster                                                 |
| deepcopy_memo              | 57.5 us                                                               | 40.8 us: 1.41x faster                                                |
| async_tree_io_tg           | 1.80 sec                                                              | 1.29 sec: 1.40x faster                                               |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 819 ms: 1.39x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.38x faster                                               |
| comprehensions             | 29.6 us                                                               | 21.7 us: 1.36x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 826 ms: 1.33x faster                                                 |
| deepcopy_reduce            | 4.45 us                                                               | 3.50 us: 1.27x faster                                                |
| raytrace                   | 418 ms                                                                | 331 ms: 1.26x faster                                                 |
| logging_format             | 11.8 us                                                               | 9.48 us: 1.25x faster                                                |
| logging_simple             | 9.89 us                                                               | 8.40 us: 1.18x faster                                                |
| sympy_str                  | 425 ms                                                                | 367 ms: 1.16x faster                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.49 ms: 1.15x faster                                                |
| generators                 | 46.0 ms                                                               | 40.2 ms: 1.15x faster                                                |
| unpickle_pure_python       | 319 us                                                                | 282 us: 1.13x faster                                                 |
| nbody                      | 125 ms                                                                | 111 ms: 1.13x faster                                                 |
| chaos                      | 93.7 ms                                                               | 83.3 ms: 1.12x faster                                                |
| xml_etree_process          | 85.7 ms                                                               | 76.7 ms: 1.12x faster                                                |
| sympy_expand               | 689 ms                                                                | 618 ms: 1.11x faster                                                 |
| deltablue                  | 5.05 ms                                                               | 4.57 ms: 1.11x faster                                                |
| regex_compile              | 197 ms                                                                | 178 ms: 1.11x faster                                                 |
| pathlib                    | 31.7 ms                                                               | 28.8 ms: 1.10x faster                                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 89.4 ms: 1.10x faster                                                |
| pycparser                  | 1.73 sec                                                              | 1.58 sec: 1.10x faster                                               |
| sqlglot_parse              | 1.89 ms                                                               | 1.73 ms: 1.09x faster                                                |
| python_startup_no_site     | 16.3 ms                                                               | 14.9 ms: 1.09x faster                                                |
| scimark_lu                 | 155 ms                                                                | 142 ms: 1.09x faster                                                 |
| tomli_loads                | 2.99 sec                                                              | 2.74 sec: 1.09x faster                                               |
| sqlglot_optimize           | 76.5 ms                                                               | 70.4 ms: 1.09x faster                                                |
| genshi_xml                 | 73.6 ms                                                               | 68.1 ms: 1.08x faster                                                |
| float                      | 127 ms                                                                | 117 ms: 1.08x faster                                                 |
| django_template            | 48.6 ms                                                               | 45.2 ms: 1.07x faster                                                |
| xml_etree_generate         | 128 ms                                                                | 120 ms: 1.07x faster                                                 |
| mako                       | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                                |
| pickle_pure_python         | 447 us                                                                | 420 us: 1.07x faster                                                 |
| mdp                        | 3.84 sec                                                              | 3.62 sec: 1.06x faster                                               |
| meteor_contest             | 149 ms                                                                | 140 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 6.28 sec: 1.06x faster                                               |
| hexiom                     | 8.87 ms                                                               | 8.41 ms: 1.05x faster                                                |
| logging_silent             | 135 ns                                                                | 128 ns: 1.05x faster                                                 |
| richards                   | 63.4 ms                                                               | 60.2 ms: 1.05x faster                                                |
| html5lib                   | 95.8 ms                                                               | 91.1 ms: 1.05x faster                                                |
| pprint_pformat             | 2.03 sec                                                              | 1.93 sec: 1.05x faster                                               |
| scimark_sor                | 171 ms                                                                | 163 ms: 1.05x faster                                                 |
| async_generators           | 617 ms                                                                | 588 ms: 1.05x faster                                                 |
| fannkuch                   | 551 ms                                                                | 528 ms: 1.04x faster                                                 |
| scimark_fft                | 499 ms                                                                | 480 ms: 1.04x faster                                                 |
| pidigits                   | 255 ms                                                                | 245 ms: 1.04x faster                                                 |
| asyncio_tcp                | 958 ms                                                                | 925 ms: 1.04x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 45.2 us: 1.03x faster                                                |
| docutils                   | 4.06 sec                                                              | 3.95 sec: 1.03x faster                                               |
| pickle                     | 14.8 us                                                               | 15.5 us: 1.04x slower                                                |
| json                       | 6.68 ms                                                               | 7.01 ms: 1.05x slower                                                |
| go                         | 185 ms                                                                | 195 ms: 1.06x slower                                                 |
| richards_super             | 67.9 ms                                                               | 71.9 ms: 1.06x slower                                                |
| create_gc_cycles           | 2.02 ms                                                               | 2.14 ms: 1.06x slower                                                |
| typing_runtime_protocols   | 199 us                                                                | 218 us: 1.09x slower                                                 |
| pickle_list                | 6.40 us                                                               | 6.99 us: 1.09x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 34.2 ms: 1.10x slower                                                |
| telco                      | 9.71 ms                                                               | 10.8 ms: 1.11x slower                                                |
| unpack_sequence            | 68.5 ns                                                               | 76.4 ns: 1.12x slower                                                |
| coverage                   | 97.6 ms                                                               | 111 ms: 1.14x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 15.7 ms: 1.16x slower                                                |
| bench_mp_pool              | 18.4 ms                                                               | 22.7 ms: 1.23x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                                         |

Benchmark hidden because not significant (28): pylint, sympy_integrate, thrift, spectral_norm, xml_etree_parse, crypto_pyaes, sympy_sum, sqlglot_normalize, gc_traversal, sqlglot_transpile, nqueens, regex_dna, 2to3, asyncio_websockets, pprint_safe_repr, regex_effbot, asyncio_tcp_ssl, json_loads, sqlite_synth, genshi_text, pyflate, python_startup, tornado_http, unpickle, coroutines, unpickle_list, xml_etree_iterparse, bench_thread_pool
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.88x