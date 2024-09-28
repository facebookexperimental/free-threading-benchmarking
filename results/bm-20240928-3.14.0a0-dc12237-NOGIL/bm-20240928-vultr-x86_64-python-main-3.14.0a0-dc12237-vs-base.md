# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc12237
- commit date: 2024-09-28
- overall geometric mean: 1.00x slower
- HPT reliability: 84.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 411 ms                                                                | 408 ms: 1.01x faster                                  |
| docutils       | 3.30 sec                                                              | 3.29 sec: 1.01x faster                                |
| html5lib       | 104 ms                                                                | 102 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization     | 518 ms                                                                | 506 ms: 1.02x faster                                  |
| async_tree_cpu_io_mixed    | 681 ms                                                                | 670 ms: 1.02x faster                                  |
| async_tree_memoization_tg  | 477 ms                                                                | 472 ms: 1.01x faster                                  |
| async_tree_cpu_io_mixed_tg | 639 ms                                                                | 635 ms: 1.01x faster                                  |
| coroutines                 | 31.2 ms                                                               | 31.4 ms: 1.01x slower                                 |
| asyncio_tcp_ssl            | 1.71 sec                                                              | 1.74 sec: 1.01x slower                                |
| async_tree_io              | 934 ms                                                                | 949 ms: 1.02x slower                                  |
| async_generators           | 482 ms                                                                | 497 ms: 1.03x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                          |

Benchmark hidden because not significant (5): async_tree_none_tg, asyncio_tcp, async_tree_none, async_tree_io_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 222 ms                                                                | 223 ms: 1.01x slower                                  |
| float          | 152 ms                                                                | 153 ms: 1.01x slower                                  |
| pidigits       | 184 ms                                                                | 188 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 193 ms                                                                | 192 ms: 1.01x faster                                  |
| regex_effbot   | 3.03 ms                                                               | 3.13 ms: 1.03x slower                                 |
| regex_v8       | 25.0 ms                                                               | 26.3 ms: 1.05x slower                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.9 ms                                                               | 13.7 ms: 1.01x faster                                 |
| unpickle_pure_python | 411 us                                                                | 408 us: 1.01x faster                                  |
| unpickle_list        | 5.13 us                                                               | 5.10 us: 1.01x faster                                 |
| xml_etree_process    | 91.2 ms                                                               | 92.0 ms: 1.01x slower                                 |
| xml_etree_iterparse  | 108 ms                                                                | 109 ms: 1.01x slower                                  |
| pickle_list          | 4.72 us                                                               | 4.77 us: 1.01x slower                                 |
| json_loads           | 28.7 us                                                               | 29.2 us: 1.02x slower                                 |
| xml_etree_parse      | 132 ms                                                                | 134 ms: 1.02x slower                                  |
| unpickle             | 14.9 us                                                               | 15.3 us: 1.02x slower                                 |
| pickle_dict          | 31.5 us                                                               | 32.6 us: 1.03x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (4): xml_etree_generate, pickle_pure_python, tomli_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 15.3 ms                                                               | 15.4 ms: 1.00x slower                                 |
| python_startup_no_site | 10.0 ms                                                               | 10.1 ms: 1.01x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| mako            | 20.5 ms                                                               | 20.4 ms: 1.01x faster                                 |
| genshi_text     | 39.2 ms                                                               | 39.5 ms: 1.01x slower                                 |
| genshi_xml      | 80.0 ms                                                               | 80.7 ms: 1.01x slower                                 |
| django_template | 63.2 ms                                                               | 64.1 ms: 1.01x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                      | 10.1 ms                                                               | 9.32 ms: 1.08x faster                                 |
| mdp                        | 3.12 sec                                                              | 3.04 sec: 1.03x faster                                |
| generators                 | 41.5 ms                                                               | 40.6 ms: 1.02x faster                                 |
| async_tree_memoization     | 518 ms                                                                | 506 ms: 1.02x faster                                  |
| meteor_contest             | 141 ms                                                                | 138 ms: 1.02x faster                                  |
| html5lib                   | 104 ms                                                                | 102 ms: 1.02x faster                                  |
| sqlite_synth               | 2.44 us                                                               | 2.39 us: 1.02x faster                                 |
| pycparser                  | 1.70 sec                                                              | 1.67 sec: 1.02x faster                                |
| async_tree_cpu_io_mixed    | 681 ms                                                                | 670 ms: 1.02x faster                                  |
| create_gc_cycles           | 1.12 ms                                                               | 1.11 ms: 1.01x faster                                 |
| logging_silent             | 213 ns                                                                | 210 ns: 1.01x faster                                  |
| raytrace                   | 642 ms                                                                | 634 ms: 1.01x faster                                  |
| json_dumps                 | 13.9 ms                                                               | 13.7 ms: 1.01x faster                                 |
| scimark_lu                 | 247 ms                                                                | 244 ms: 1.01x faster                                  |
| coverage                   | 105 ms                                                                | 104 ms: 1.01x faster                                  |
| async_tree_memoization_tg  | 477 ms                                                                | 472 ms: 1.01x faster                                  |
| logging_format             | 13.2 us                                                               | 13.1 us: 1.01x faster                                 |
| logging_simple             | 12.0 us                                                               | 11.9 us: 1.01x faster                                 |
| dulwich_log                | 104 ms                                                                | 103 ms: 1.01x faster                                  |
| regex_dna                  | 193 ms                                                                | 192 ms: 1.01x faster                                  |
| async_tree_cpu_io_mixed_tg | 639 ms                                                                | 635 ms: 1.01x faster                                  |
| mako                       | 20.5 ms                                                               | 20.4 ms: 1.01x faster                                 |
| 2to3                       | 411 ms                                                                | 408 ms: 1.01x faster                                  |
| unpickle_pure_python       | 411 us                                                                | 408 us: 1.01x faster                                  |
| unpickle_list              | 5.13 us                                                               | 5.10 us: 1.01x faster                                 |
| gc_traversal               | 2.46 ms                                                               | 2.44 ms: 1.01x faster                                 |
| docutils                   | 3.30 sec                                                              | 3.29 sec: 1.01x faster                                |
| pyflate                    | 773 ms                                                                | 775 ms: 1.00x slower                                  |
| sympy_expand               | 1.05 sec                                                              | 1.05 sec: 1.00x slower                                |
| sympy_integrate            | 32.3 ms                                                               | 32.4 ms: 1.00x slower                                 |
| python_startup             | 15.3 ms                                                               | 15.4 ms: 1.00x slower                                 |
| pprint_pformat             | 2.71 sec                                                              | 2.72 sec: 1.01x slower                                |
| python_startup_no_site     | 10.0 ms                                                               | 10.1 ms: 1.01x slower                                 |
| bench_mp_pool              | 70.4 ms                                                               | 70.7 ms: 1.01x slower                                 |
| comprehensions             | 30.0 us                                                               | 30.1 us: 1.01x slower                                 |
| crypto_pyaes               | 108 ms                                                                | 109 ms: 1.01x slower                                  |
| scimark_sparse_mat_mult    | 6.32 ms                                                               | 6.36 ms: 1.01x slower                                 |
| nbody                      | 222 ms                                                                | 223 ms: 1.01x slower                                  |
| genshi_text                | 39.2 ms                                                               | 39.5 ms: 1.01x slower                                 |
| scimark_monte_carlo        | 128 ms                                                                | 129 ms: 1.01x slower                                  |
| coroutines                 | 31.2 ms                                                               | 31.4 ms: 1.01x slower                                 |
| sqlglot_normalize          | 176 ms                                                                | 177 ms: 1.01x slower                                  |
| xml_etree_process          | 91.2 ms                                                               | 92.0 ms: 1.01x slower                                 |
| float                      | 152 ms                                                                | 153 ms: 1.01x slower                                  |
| genshi_xml                 | 80.0 ms                                                               | 80.7 ms: 1.01x slower                                 |
| sqlglot_parse              | 2.84 ms                                                               | 2.86 ms: 1.01x slower                                 |
| xml_etree_iterparse        | 108 ms                                                                | 109 ms: 1.01x slower                                  |
| deepcopy_memo              | 52.4 us                                                               | 53.0 us: 1.01x slower                                 |
| richards_super             | 106 ms                                                                | 107 ms: 1.01x slower                                  |
| pickle_list                | 4.72 us                                                               | 4.77 us: 1.01x slower                                 |
| sqlglot_transpile          | 3.29 ms                                                               | 3.33 ms: 1.01x slower                                 |
| deepcopy_reduce            | 4.46 us                                                               | 4.52 us: 1.01x slower                                 |
| json                       | 5.26 ms                                                               | 5.33 ms: 1.01x slower                                 |
| asyncio_tcp_ssl            | 1.71 sec                                                              | 1.74 sec: 1.01x slower                                |
| deepcopy                   | 425 us                                                                | 430 us: 1.01x slower                                  |
| fannkuch                   | 569 ms                                                                | 577 ms: 1.01x slower                                  |
| django_template            | 63.2 ms                                                               | 64.1 ms: 1.01x slower                                 |
| async_tree_io              | 934 ms                                                                | 949 ms: 1.02x slower                                  |
| json_loads                 | 28.7 us                                                               | 29.2 us: 1.02x slower                                 |
| pathlib                    | 21.7 ms                                                               | 22.0 ms: 1.02x slower                                 |
| xml_etree_parse            | 132 ms                                                                | 134 ms: 1.02x slower                                  |
| scimark_fft                | 450 ms                                                                | 458 ms: 1.02x slower                                  |
| nqueens                    | 116 ms                                                                | 119 ms: 1.02x slower                                  |
| pidigits                   | 184 ms                                                                | 188 ms: 1.02x slower                                  |
| unpickle                   | 14.9 us                                                               | 15.3 us: 1.02x slower                                 |
| spectral_norm              | 172 ms                                                                | 177 ms: 1.02x slower                                  |
| async_generators           | 482 ms                                                                | 497 ms: 1.03x slower                                  |
| regex_effbot               | 3.03 ms                                                               | 3.13 ms: 1.03x slower                                 |
| pickle_dict                | 31.5 us                                                               | 32.6 us: 1.03x slower                                 |
| go                         | 289 ms                                                                | 301 ms: 1.04x slower                                  |
| regex_v8                   | 25.0 ms                                                               | 26.3 ms: 1.05x slower                                 |
| unpack_sequence            | 134 ns                                                                | 149 ns: 1.12x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                          |

Benchmark hidden because not significant (25): async_tree_none_tg, pylint, scimark_sor, typing_runtime_protocols, xml_etree_generate, chaos, tornado_http, asyncio_tcp, pickle_pure_python, bench_thread_pool, thrift, deltablue, sympy_sum, async_tree_none, async_tree_io_tg, sympy_str, bpe_tokeniser, asyncio_websockets, richards, hexiom, sqlglot_optimize, regex_compile, pprint_safe_repr, tomli_loads, pickle

# HPT report

- Reliability score: 84.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x