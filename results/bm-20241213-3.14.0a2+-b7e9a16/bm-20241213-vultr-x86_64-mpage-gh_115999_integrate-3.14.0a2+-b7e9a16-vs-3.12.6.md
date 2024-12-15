# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                 |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                 |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.43x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                |
| async_generators           | 384 ms                                                 | 354 ms: 1.08x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                 |
| nbody          | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                 |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                               |
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                                 |
| json_loads           | 26.5 us                                                | 26.2 us: 1.01x faster                                                |
| xml_etree_process    | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.04x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                 |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.43x faster                                                 |
| deepcopy                   | 352 us                                                 | 252 us: 1.39x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 30.1 us: 1.34x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.17x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                |
| raytrace                   | 299 ms                                                 | 258 ms: 1.16x faster                                                 |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.24 sec: 1.12x faster                                               |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.14 ms: 1.10x faster                                                |
| spectral_norm              | 110 ms                                                 | 100 ms: 1.10x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.06 us: 1.09x faster                                                |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                |
| logging_format             | 7.35 us                                                | 6.74 us: 1.09x faster                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                |
| async_generators           | 384 ms                                                 | 354 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.08x faster                                                |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                 |
| scimark_fft                | 342 ms                                                 | 317 ms: 1.08x faster                                                 |
| thrift                     | 791 us                                                 | 737 us: 1.07x faster                                                 |
| chaos                      | 62.8 ms                                                | 58.5 ms: 1.07x faster                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.76 ms: 1.07x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                |
| richards                   | 45.9 ms                                                | 43.2 ms: 1.06x faster                                                |
| float                      | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.15 ms: 1.06x faster                                                |
| json                       | 5.02 ms                                                | 4.75 ms: 1.06x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                                 |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                               |
| pyflate                    | 448 ms                                                 | 429 ms: 1.04x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.04x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                                |
| dulwich_log                | 78.9 ms                                                | 75.7 ms: 1.04x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                               |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                               |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.04x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.9 ms: 1.04x faster                                                |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 718 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                               |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.8 ms: 1.03x faster                                                |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.9 ms: 1.03x faster                                                |
| json_loads                 | 26.5 us                                                | 26.2 us: 1.01x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                 |
| nbody                      | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                |
| telco                      | 6.53 ms                                                | 7.25 ms: 1.11x slower                                                |
| coverage                   | 71.4 ms                                                | 79.4 ms: 1.11x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                |
| gc_traversal               | 3.46 ms                                                | 4.46 ms: 1.29x slower                                                |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 88.7 ms: 8.21x slower                                                |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                         |

Benchmark hidden because not significant (3): sqlite_synth, xml_etree_generate, fannkuch
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x