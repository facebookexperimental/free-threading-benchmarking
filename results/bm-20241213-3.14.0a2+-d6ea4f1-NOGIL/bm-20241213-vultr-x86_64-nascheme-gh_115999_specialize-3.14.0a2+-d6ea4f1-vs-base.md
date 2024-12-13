# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.033x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 365 ms: 1.01x faster                                                     |
| html5lib       | 97.9 ms                                                                | 95.0 ms: 1.03x faster                                                    |
| sphinx         | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 358 ms                                                                 | 329 ms: 1.09x faster                                                     |
| async_tree_io_tg           | 822 ms                                                                 | 765 ms: 1.07x faster                                                     |
| async_tree_none            | 388 ms                                                                 | 362 ms: 1.07x faster                                                     |
| async_tree_memoization_tg  | 445 ms                                                                 | 420 ms: 1.06x faster                                                     |
| async_tree_io              | 841 ms                                                                 | 793 ms: 1.06x faster                                                     |
| async_tree_memoization     | 469 ms                                                                 | 446 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 593 ms: 1.04x faster                                                     |
| async_generators           | 456 ms                                                                 | 438 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 620 ms: 1.03x faster                                                     |
| coroutines                 | 24.9 ms                                                                | 24.1 ms: 1.03x faster                                                    |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 137 ms                                                                 | 113 ms: 1.21x faster                                                     |
| nbody          | 128 ms                                                                 | 126 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                 | 172 ms: 1.05x faster                                                     |
| regex_effbot   | 2.79 ms                                                                | 2.80 ms: 1.00x slower                                                    |
| regex_dna      | 182 ms                                                                 | 183 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 77.9 ms                                                                | 73.1 ms: 1.07x faster                                                    |
| pickle_pure_python   | 515 us                                                                 | 492 us: 1.05x faster                                                     |
| tomli_loads          | 2.67 sec                                                               | 2.60 sec: 1.03x faster                                                   |
| unpickle_pure_python | 333 us                                                                 | 326 us: 1.02x faster                                                     |
| xml_etree_iterparse  | 91.3 ms                                                                | 90.4 ms: 1.01x faster                                                    |
| json_dumps           | 14.2 ms                                                                | 14.1 ms: 1.01x faster                                                    |
| xml_etree_generate   | 97.3 ms                                                                | 96.5 ms: 1.01x faster                                                    |
| xml_etree_parse      | 131 ms                                                                 | 131 ms: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 31.9 ms                                                                | 31.2 ms: 1.02x faster                                                    |
| genshi_xml      | 63.8 ms                                                                | 62.9 ms: 1.02x faster                                                    |
| django_template | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                    |
| mako            | 17.7 ms                                                                | 17.6 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 137 ms                                                                 | 113 ms: 1.21x faster                                                     |
| richards                   | 76.7 ms                                                                | 66.8 ms: 1.15x faster                                                    |
| richards_super             | 86.2 ms                                                                | 75.4 ms: 1.14x faster                                                    |
| thrift                     | 1.16 ms                                                                | 1.03 ms: 1.13x faster                                                    |
| scimark_monte_carlo        | 118 ms                                                                 | 105 ms: 1.13x faster                                                     |
| scimark_sparse_mat_mult    | 6.04 ms                                                                | 5.39 ms: 1.12x faster                                                    |
| raytrace                   | 547 ms                                                                 | 489 ms: 1.12x faster                                                     |
| sqlglot_parse              | 2.58 ms                                                                | 2.33 ms: 1.11x faster                                                    |
| go                         | 267 ms                                                                 | 241 ms: 1.11x faster                                                     |
| chaos                      | 104 ms                                                                 | 95.0 ms: 1.09x faster                                                    |
| sqlglot_transpile          | 2.93 ms                                                                | 2.69 ms: 1.09x faster                                                    |
| deltablue                  | 8.00 ms                                                                | 7.35 ms: 1.09x faster                                                    |
| async_tree_none_tg         | 358 ms                                                                 | 329 ms: 1.09x faster                                                     |
| logging_format             | 12.0 us                                                                | 11.1 us: 1.08x faster                                                    |
| pycparser                  | 1.55 sec                                                               | 1.43 sec: 1.08x faster                                                   |
| async_tree_io_tg           | 822 ms                                                                 | 765 ms: 1.07x faster                                                     |
| async_tree_none            | 388 ms                                                                 | 362 ms: 1.07x faster                                                     |
| xml_etree_process          | 77.9 ms                                                                | 73.1 ms: 1.07x faster                                                    |
| async_tree_memoization_tg  | 445 ms                                                                 | 420 ms: 1.06x faster                                                     |
| async_tree_io              | 841 ms                                                                 | 793 ms: 1.06x faster                                                     |
| logging_simple             | 10.6 us                                                                | 9.97 us: 1.06x faster                                                    |
| async_tree_memoization     | 469 ms                                                                 | 446 ms: 1.05x faster                                                     |
| sqlite_synth               | 2.29 us                                                                | 2.18 us: 1.05x faster                                                    |
| sqlalchemy_imperative      | 29.8 ms                                                                | 28.5 ms: 1.05x faster                                                    |
| regex_compile              | 180 ms                                                                 | 172 ms: 1.05x faster                                                     |
| pickle_pure_python         | 515 us                                                                 | 492 us: 1.05x faster                                                     |
| async_tree_cpu_io_mixed_tg | 618 ms                                                                 | 593 ms: 1.04x faster                                                     |
| async_generators           | 456 ms                                                                 | 438 ms: 1.04x faster                                                     |
| subparsers                 | 31.6 ms                                                                | 30.3 ms: 1.04x faster                                                    |
| pyflate                    | 699 ms                                                                 | 673 ms: 1.04x faster                                                     |
| scimark_fft                | 398 ms                                                                 | 384 ms: 1.03x faster                                                     |
| dulwich_log                | 95.9 ms                                                                | 92.9 ms: 1.03x faster                                                    |
| html5lib                   | 97.9 ms                                                                | 95.0 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 620 ms: 1.03x faster                                                     |
| coroutines                 | 24.9 ms                                                                | 24.1 ms: 1.03x faster                                                    |
| logging_silent             | 185 ns                                                                 | 180 ns: 1.03x faster                                                     |
| hexiom                     | 9.88 ms                                                                | 9.63 ms: 1.03x faster                                                    |
| tomli_loads                | 2.67 sec                                                               | 2.60 sec: 1.03x faster                                                   |
| scimark_sor                | 236 ms                                                                 | 230 ms: 1.02x faster                                                     |
| scimark_lu                 | 184 ms                                                                 | 180 ms: 1.02x faster                                                     |
| crypto_pyaes               | 92.1 ms                                                                | 90.0 ms: 1.02x faster                                                    |
| genshi_text                | 31.9 ms                                                                | 31.2 ms: 1.02x faster                                                    |
| comprehensions             | 27.4 us                                                                | 26.8 us: 1.02x faster                                                    |
| spectral_norm              | 123 ms                                                                 | 120 ms: 1.02x faster                                                     |
| deepcopy_memo              | 39.6 us                                                                | 38.8 us: 1.02x faster                                                    |
| typing_runtime_protocols   | 203 us                                                                 | 199 us: 1.02x faster                                                     |
| unpickle_pure_python       | 333 us                                                                 | 326 us: 1.02x faster                                                     |
| sqlalchemy_declarative     | 203 ms                                                                 | 199 ms: 1.02x faster                                                     |
| nbody                      | 128 ms                                                                 | 126 ms: 1.02x faster                                                     |
| telco                      | 8.84 ms                                                                | 8.70 ms: 1.02x faster                                                    |
| genshi_xml                 | 63.8 ms                                                                | 62.9 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 3.49 us                                                                | 3.45 us: 1.01x faster                                                    |
| create_gc_cycles           | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                                    |
| django_template            | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.99 sec                                                               | 4.93 sec: 1.01x faster                                                   |
| xml_etree_iterparse        | 91.3 ms                                                                | 90.4 ms: 1.01x faster                                                    |
| generators                 | 38.0 ms                                                                | 37.6 ms: 1.01x faster                                                    |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                     |
| pprint_pformat             | 2.02 sec                                                               | 2.00 sec: 1.01x faster                                                   |
| json_dumps                 | 14.2 ms                                                                | 14.1 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 970 ms                                                                 | 962 ms: 1.01x faster                                                     |
| xml_etree_generate         | 97.3 ms                                                                | 96.5 ms: 1.01x faster                                                    |
| sympy_sum                  | 350 ms                                                                 | 348 ms: 1.01x faster                                                     |
| sphinx                     | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| xml_etree_parse            | 131 ms                                                                 | 131 ms: 1.01x faster                                                     |
| mako                       | 17.7 ms                                                                | 17.6 ms: 1.01x faster                                                    |
| 2to3                       | 367 ms                                                                 | 365 ms: 1.01x faster                                                     |
| fannkuch                   | 495 ms                                                                 | 492 ms: 1.01x faster                                                     |
| gc_traversal               | 3.54 ms                                                                | 3.52 ms: 1.01x faster                                                    |
| nqueens                    | 97.4 ms                                                                | 96.8 ms: 1.01x faster                                                    |
| python_startup             | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                                    |
| deepcopy                   | 324 us                                                                 | 323 us: 1.00x faster                                                     |
| k_core                     | 2.42 sec                                                               | 2.41 sec: 1.00x faster                                                   |
| sympy_expand               | 955 ms                                                                 | 952 ms: 1.00x faster                                                     |
| sympy_integrate            | 29.6 ms                                                                | 29.5 ms: 1.00x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| regex_effbot               | 2.79 ms                                                                | 2.80 ms: 1.00x slower                                                    |
| json                       | 5.02 ms                                                                | 5.05 ms: 1.01x slower                                                    |
| regex_dna                  | 182 ms                                                                 | 183 ms: 1.01x slower                                                     |
| coverage                   | 99.5 ms                                                                | 104 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (16): pylint, regex_v8, sqlglot_optimize, meteor_contest, sympy_str, bench_thread_pool, pathlib, docutils, connected_components, mdp, asyncio_websockets, shortest_path, sqlglot_normalize, pidigits, json_loads, many_optionals

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x