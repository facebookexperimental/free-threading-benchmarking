# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 9015a3f
- commit date: 2024-12-18
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 630 ms: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 277 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                     |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 76.5 ms: 1.01x faster                                                    |
| pidigits       | 217 ms                                                       | 222 ms: 1.03x slower                                                     |
| nbody          | 85.1 ms                                                      | 89.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 169 ms: 1.07x faster                                                     |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                        | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                    |
| json_loads           | 27.0 us                                                      | 26.0 us: 1.04x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                    |
| genshi_xml      | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                    |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                    |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                     |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                     |
| async_tree_io              | 876 ms                                                       | 630 ms: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 29.3 us: 1.33x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 277 ms: 1.27x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                                    |
| go                         | 141 ms                                                       | 116 ms: 1.21x faster                                                     |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| spectral_norm              | 111 ms                                                       | 99.0 ms: 1.12x faster                                                    |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.22 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.16 ms: 1.09x faster                                                    |
| generators                 | 28.8 ms                                                      | 26.8 ms: 1.08x faster                                                    |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                     |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.07x faster                                                     |
| pyflate                    | 449 ms                                                       | 420 ms: 1.07x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                    |
| scimark_sor                | 134 ms                                                       | 128 ms: 1.05x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.25 sec: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.5 ms: 1.05x faster                                                    |
| coverage                   | 83.0 ms                                                      | 79.4 ms: 1.05x faster                                                    |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| thrift                     | 778 us                                                       | 746 us: 1.04x faster                                                     |
| richards                   | 45.2 ms                                                      | 43.5 ms: 1.04x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 710 ms: 1.04x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.77 ms: 1.04x faster                                                    |
| json_loads                 | 27.0 us                                                      | 26.0 us: 1.04x faster                                                    |
| json                       | 4.93 ms                                                      | 4.75 ms: 1.04x faster                                                    |
| richards_super             | 51.6 ms                                                      | 49.9 ms: 1.04x faster                                                    |
| meteor_contest             | 102 ms                                                       | 98.2 ms: 1.03x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                    |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                   |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                     |
| tomli_loads                | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.4 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| 2to3                       | 260 ms                                                       | 256 ms: 1.01x faster                                                     |
| float                      | 77.5 ms                                                      | 76.5 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 52.1 ms: 1.01x faster                                                    |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                     |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                    |
| fannkuch                   | 370 ms                                                       | 371 ms: 1.00x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.00x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 75.2 ms: 1.00x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.20 us: 1.01x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.57 ms: 1.01x slower                                                    |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                     |
| logging_format             | 6.84 us                                                      | 6.90 us: 1.01x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                    |
| raytrace                   | 253 ms                                                       | 256 ms: 1.02x slower                                                     |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                    |
| pidigits                   | 217 ms                                                       | 222 ms: 1.03x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.44 sec: 1.04x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.1 us: 1.04x slower                                                    |
| nbody                      | 85.1 ms                                                      | 89.1 ms: 1.05x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.19 ms: 1.33x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 88.5 ms: 8.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                             |

Benchmark hidden because not significant (6): sympy_str, chaos, sympy_integrate, sqlite_synth, sympy_expand, deltablue
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241218-3.14.0a3+-9015a3f/bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x