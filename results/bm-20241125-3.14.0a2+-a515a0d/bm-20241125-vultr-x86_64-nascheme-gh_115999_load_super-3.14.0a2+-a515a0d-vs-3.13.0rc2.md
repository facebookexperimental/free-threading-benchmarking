# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.001x faster
- HPT reliability: 73.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 570 ms: 1.17x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 407 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 568 ms: 1.12x faster                                                     |
| async_tree_none            | 354 ms                                                       | 332 ms: 1.06x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 889 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                             |

Benchmark hidden because not significant (3): async_tree_io, async_generators, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                     |
| float          | 77.5 ms                                                      | 79.7 ms: 1.03x slower                                                    |
| nbody          | 85.1 ms                                                      | 94.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                    |
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                                     |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                        | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.8 us: 1.09x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 137 ms: 1.00x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 86.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.3 ms: 1.04x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 321 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                        | 1.15x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                    |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.7 ms: 1.04x slower                                                    |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deepcopy                   | 355 us                                                       | 262 us: 1.36x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.5 us: 1.28x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                    |
| pylint                     | 317 ms                                                       | 270 ms: 1.17x faster                                                     |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                     |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 570 ms: 1.17x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 407 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 568 ms: 1.12x faster                                                     |
| json_loads                 | 27.0 us                                                      | 24.8 us: 1.09x faster                                                    |
| json                       | 4.93 ms                                                      | 4.56 ms: 1.08x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                    |
| async_tree_none            | 354 ms                                                       | 332 ms: 1.06x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.37 ms: 1.06x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                    |
| scimark_fft                | 349 ms                                                       | 336 ms: 1.04x faster                                                     |
| thrift                     | 778 us                                                       | 752 us: 1.04x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 889 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 720 ms: 1.02x faster                                                     |
| regex_compile              | 132 ms                                                       | 129 ms: 1.02x faster                                                     |
| meteor_contest             | 102 ms                                                       | 99.7 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 67.0 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.2 ms: 1.01x faster                                                    |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.94 ms: 1.01x faster                                                    |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                   |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x slower                                                     |
| xml_etree_parse            | 136 ms                                                       | 137 ms: 1.00x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 78.9 ms: 1.00x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| richards_super             | 51.6 ms                                                      | 51.9 ms: 1.01x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 65.8 ms: 1.01x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 86.0 ms: 1.01x slower                                                    |
| richards                   | 45.2 ms                                                      | 45.6 ms: 1.01x slower                                                    |
| sympy_expand               | 457 ms                                                       | 461 ms: 1.01x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.01x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 53.6 ms: 1.02x slower                                                    |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                     |
| logging_simple             | 6.16 us                                                      | 6.30 us: 1.02x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                    |
| scimark_sor                | 134 ms                                                       | 138 ms: 1.03x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                     |
| chaos                      | 57.3 ms                                                      | 58.9 ms: 1.03x slower                                                    |
| float                      | 77.5 ms                                                      | 79.7 ms: 1.03x slower                                                    |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| generators                 | 28.8 ms                                                      | 29.8 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 98.3 ms: 1.04x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.7 ms: 1.04x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.25 ms: 1.04x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.13 us: 1.04x slower                                                    |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                                     |
| django_template            | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                   |
| raytrace                   | 253 ms                                                       | 267 ms: 1.06x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.50 sec: 1.06x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.06x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 321 us: 1.09x slower                                                     |
| nbody                      | 85.1 ms                                                      | 94.2 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.24 ms: 1.35x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 86.2 ms: 7.84x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                             |

Benchmark hidden because not significant (8): async_tree_io, scimark_sparse_mat_mult, scimark_lu, pyflate, async_generators, python_startup_no_site, sqlite_synth, async_tree_none_tg
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241125-3.14.0a2+-a515a0d/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.001x faster
# HPT report

- Reliability score: 73.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x