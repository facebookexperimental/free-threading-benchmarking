# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 319 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 545 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                  |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                  |
| coroutines                 | 23.9 ms                                                | 20.8 ms: 1.15x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                 |
| pidigits       | 184 ms                                                 | 211 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.06x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                 |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.9 ms: 1.07x faster                                                 |
| django_template | 34.7 ms                                                | 33.7 ms: 1.03x faster                                                 |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 319 ms: 1.74x faster                                                  |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.3 us: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 545 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                  |
| go                         | 139 ms                                                 | 114 ms: 1.23x faster                                                  |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                  |
| generators                 | 32.2 ms                                                | 26.6 ms: 1.21x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.6 us: 1.19x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                  |
| coroutines                 | 23.9 ms                                                | 20.8 ms: 1.15x faster                                                 |
| spectral_norm              | 110 ms                                                 | 95.9 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.14x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                 |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                                |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.06 ms: 1.13x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                                  |
| pyflate                    | 448 ms                                                 | 402 ms: 1.11x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                  |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                                |
| richards                   | 45.9 ms                                                | 42.0 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.6 ms: 1.09x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 681 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                  |
| thrift                     | 791 us                                                 | 727 us: 1.09x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.7 ms: 1.09x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.72 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 46.9 ms: 1.07x faster                                                 |
| meteor_contest             | 104 ms                                                 | 96.9 ms: 1.07x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.06x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.5 ms: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 101 ms: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.2 ms: 1.05x faster                                                 |
| sympy_expand               | 468 ms                                                 | 448 ms: 1.05x faster                                                  |
| nqueens                    | 80.1 ms                                                | 76.9 ms: 1.04x faster                                                 |
| mdp                        | 2.42 sec                                               | 2.33 sec: 1.04x faster                                                |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| sqlglot_optimize           | 53.3 ms                                                | 51.4 ms: 1.04x faster                                                 |
| django_template            | 34.7 ms                                                | 33.7 ms: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                 |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.33 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                 |
| telco                      | 6.53 ms                                                | 7.09 ms: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                 |
| pidigits                   | 184 ms                                                 | 211 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.28 ms: 1.24x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.2 ms: 8.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): nbody
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250115-3.14.0a4+-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.11x