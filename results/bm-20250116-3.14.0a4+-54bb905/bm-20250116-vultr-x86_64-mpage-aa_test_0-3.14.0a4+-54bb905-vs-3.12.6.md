# Results vs. 3.12.6

- fork: mpage
- ref: aa_test_0
- machine: linux-x86_64
- commit hash: 54bb905
- commit date: 2025-01-16
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                       |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                       |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 565 ms: 1.28x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 587 ms: 1.22x faster                                       |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                       |
| coroutines                 | 23.9 ms                                                | 21.2 ms: 1.13x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.45x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.0 ms: 1.11x faster                                      |
| nbody          | 89.3 ms                                                | 88.3 ms: 1.01x faster                                      |
| pidigits       | 184 ms                                                 | 227 ms: 1.23x slower                                       |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                      |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                       |
| regex_v8       | 20.6 ms                                                | 24.8 ms: 1.20x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                     |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                      |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                       |
| xml_etree_process    | 59.0 ms                                                | 60.0 ms: 1.02x slower                                      |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                      |
| pickle_pure_python   | 308 us                                                 | 320 us: 1.04x slower                                       |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.43 ms: 1.04x slower                                      |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                      |
| Geometric mean         | (ref)                                                  | 1.24x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                      |
| genshi_xml      | 50.2 ms                                                | 49.5 ms: 1.01x faster                                      |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                      |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                      |
| Geometric mean  | (ref)                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                       |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                       |
| deepcopy                   | 352 us                                                 | 259 us: 1.36x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 565 ms: 1.28x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 587 ms: 1.22x faster                                       |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                      |
| spectral_norm              | 110 ms                                                 | 92.3 ms: 1.19x faster                                      |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                       |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.18x faster                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                      |
| crypto_pyaes               | 76.6 ms                                                | 66.2 ms: 1.16x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                      |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                      |
| chaos                      | 62.8 ms                                                | 55.6 ms: 1.13x faster                                      |
| coroutines                 | 23.9 ms                                                | 21.2 ms: 1.13x faster                                      |
| raytrace                   | 299 ms                                                 | 266 ms: 1.13x faster                                       |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.12x faster                                       |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                       |
| float                      | 80.8 ms                                                | 73.0 ms: 1.11x faster                                      |
| pyflate                    | 448 ms                                                 | 405 ms: 1.11x faster                                       |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                     |
| deltablue                  | 3.45 ms                                                | 3.14 ms: 1.10x faster                                      |
| richards                   | 45.9 ms                                                | 42.0 ms: 1.09x faster                                      |
| generators                 | 32.2 ms                                                | 29.5 ms: 1.09x faster                                      |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                       |
| scimark_fft                | 342 ms                                                 | 317 ms: 1.08x faster                                       |
| richards_super             | 51.9 ms                                                | 48.1 ms: 1.08x faster                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 63.8 ms: 1.07x faster                                      |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                       |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                      |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                      |
| logging_simple             | 6.63 us                                                | 6.20 us: 1.07x faster                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.07x faster                                      |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                       |
| thrift                     | 791 us                                                 | 742 us: 1.07x faster                                       |
| hexiom                     | 6.17 ms                                                | 5.79 ms: 1.07x faster                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                      |
| logging_format             | 7.35 us                                                | 6.97 us: 1.05x faster                                      |
| pprint_safe_repr           | 743 ms                                                 | 706 ms: 1.05x faster                                       |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                     |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                     |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                       |
| meteor_contest             | 104 ms                                                 | 99.9 ms: 1.04x faster                                      |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                       |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                      |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                       |
| dulwich_log                | 78.9 ms                                                | 76.6 ms: 1.03x faster                                      |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                     |
| mdp                        | 2.42 sec                                               | 2.37 sec: 1.02x faster                                     |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                       |
| genshi_xml                 | 50.2 ms                                                | 49.5 ms: 1.01x faster                                      |
| nqueens                    | 80.1 ms                                                | 79.1 ms: 1.01x faster                                      |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                       |
| nbody                      | 89.3 ms                                                | 88.3 ms: 1.01x faster                                      |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                       |
| sqlglot_optimize           | 53.3 ms                                                | 52.8 ms: 1.01x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 60.0 ms: 1.02x slower                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.48 ms: 1.02x slower                                      |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 7.43 ms: 1.04x slower                                      |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                      |
| pickle_pure_python         | 308 us                                                 | 320 us: 1.04x slower                                       |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                      |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                      |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| telco                      | 6.53 ms                                                | 7.18 ms: 1.10x slower                                      |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                      |
| coverage                   | 71.4 ms                                                | 79.8 ms: 1.12x slower                                      |
| regex_v8                   | 20.6 ms                                                | 24.8 ms: 1.20x slower                                      |
| gc_traversal               | 3.46 ms                                                | 4.21 ms: 1.22x slower                                      |
| pidigits                   | 184 ms                                                 | 227 ms: 1.23x slower                                       |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 88.6 ms: 8.20x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (4): json, fannkuch, xml_etree_generate, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4+-54bb905.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x