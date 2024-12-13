# Results vs. 3.12.6

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| nbody          | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| regex_compile  | 142 ms                                                 | 128 ms: 1.11x faster                                                   |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.06 sec: 1.02x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.9 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 26.2 us: 1.01x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| django_template | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.7 us: 1.36x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 18.8 ms: 1.16x faster                                                  |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.2 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.95 us: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.61 us: 1.11x faster                                                  |
| regex_compile              | 142 ms                                                 | 128 ms: 1.11x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.5 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.7 ms: 1.07x faster                                                  |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 699 ms: 1.06x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.81 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| json                       | 5.02 ms                                                | 4.74 ms: 1.06x faster                                                  |
| thrift                     | 791 us                                                 | 750 us: 1.06x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| meteor_contest             | 104 ms                                                 | 98.6 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.59 ms: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| float                      | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.03x faster                                                   |
| sympy_expand               | 468 ms                                                 | 455 ms: 1.03x faster                                                   |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.06 sec: 1.02x faster                                                 |
| scimark_fft                | 342 ms                                                 | 335 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 52.4 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.9 ms: 1.02x faster                                                  |
| json_loads                 | 26.5 us                                                | 26.2 us: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| richards                   | 45.9 ms                                                | 45.4 ms: 1.01x faster                                                  |
| richards_super             | 51.9 ms                                                | 51.4 ms: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                                   |
| pyflate                    | 448 ms                                                 | 445 ms: 1.01x faster                                                   |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x slower                                                   |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| django_template            | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                  |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.47 sec: 1.02x slower                                                 |
| nbody                      | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                  |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.3 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.26 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.41 ms: 1.28x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.8 ms: 8.22x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): genshi_xml
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x