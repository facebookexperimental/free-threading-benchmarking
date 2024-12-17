# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.250x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 360 ms: 1.41x slower                                                     |
| docutils       | 2.55 sec                                                               | 3.05 sec: 1.20x slower                                                   |
| sphinx         | 992 ms                                                                 | 1.16 sec: 1.17x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.25x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                     |
| coroutines                 | 21.6 ms                                                                | 24.1 ms: 1.12x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 574 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 598 ms: 1.20x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 740 ms: 1.21x slower                                                     |
| async_tree_io              | 627 ms                                                                 | 761 ms: 1.21x slower                                                     |
| async_tree_none_tg         | 256 ms                                                                 | 322 ms: 1.26x slower                                                     |
| async_generators           | 352 ms                                                                 | 444 ms: 1.26x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 354 ms: 1.28x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 429 ms: 1.29x slower                                                     |
| async_tree_memoization_tg  | 307 ms                                                                 | 401 ms: 1.30x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.21x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 90.3 ms                                                                | 131 ms: 1.45x slower                                                     |
| float          | 76.4 ms                                                                | 111 ms: 1.45x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 25.0 ms: 1.03x slower                                                    |
| regex_effbot   | 2.69 ms                                                                | 2.97 ms: 1.10x slower                                                    |
| regex_dna      | 175 ms                                                                 | 192 ms: 1.10x slower                                                     |
| regex_compile  | 127 ms                                                                 | 170 ms: 1.34x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.02x slower                                                     |
| json_loads           | 26.1 us                                                                | 28.5 us: 1.09x slower                                                    |
| xml_etree_generate   | 84.5 ms                                                                | 97.6 ms: 1.15x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 14.2 ms: 1.25x slower                                                    |
| xml_etree_process    | 58.8 ms                                                                | 73.8 ms: 1.25x slower                                                    |
| tomli_loads          | 1.97 sec                                                               | 2.58 sec: 1.31x slower                                                   |
| pickle_pure_python   | 323 us                                                                 | 502 us: 1.55x slower                                                     |
| unpickle_pure_python | 213 us                                                                 | 331 us: 1.56x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.7 ms                                                                | 63.7 ms: 1.28x slower                                                    |
| django_template | 35.4 ms                                                                | 50.2 ms: 1.42x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 30.9 ms: 1.43x slower                                                    |
| mako            | 11.6 ms                                                                | 17.2 ms: 1.48x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                | 3.15 ms: 1.36x faster                                                    |
| create_gc_cycles           | 1.83 ms                                                                | 1.78 ms: 1.03x faster                                                    |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                     |
| sqlite_synth               | 2.20 us                                                                | 2.16 us: 1.02x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                     |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.02x slower                                                     |
| regex_v8                   | 24.4 ms                                                                | 25.0 ms: 1.03x slower                                                    |
| json                       | 4.76 ms                                                                | 5.07 ms: 1.06x slower                                                    |
| json_loads                 | 26.1 us                                                                | 28.5 us: 1.09x slower                                                    |
| pathlib                    | 18.2 ms                                                                | 19.9 ms: 1.09x slower                                                    |
| regex_effbot               | 2.69 ms                                                                | 2.97 ms: 1.10x slower                                                    |
| regex_dna                  | 175 ms                                                                 | 192 ms: 1.10x slower                                                     |
| coroutines                 | 21.6 ms                                                                | 24.1 ms: 1.12x slower                                                    |
| spectral_norm              | 96.3 ms                                                                | 110 ms: 1.14x slower                                                     |
| k_core                     | 2.05 sec                                                               | 2.36 sec: 1.15x slower                                                   |
| xml_etree_generate         | 84.5 ms                                                                | 97.6 ms: 1.15x slower                                                    |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                    |
| sphinx                     | 992 ms                                                                 | 1.16 sec: 1.17x slower                                                   |
| dulwich_log                | 76.6 ms                                                                | 90.8 ms: 1.19x slower                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 574 ms: 1.19x slower                                                     |
| bpe_tokeniser              | 4.24 sec                                                               | 5.03 sec: 1.19x slower                                                   |
| docutils                   | 2.55 sec                                                               | 3.05 sec: 1.20x slower                                                   |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 598 ms: 1.20x slower                                                     |
| telco                      | 7.18 ms                                                                | 8.64 ms: 1.20x slower                                                    |
| bench_mp_pool              | 88.9 ms                                                                | 107 ms: 1.20x slower                                                     |
| async_tree_io_tg           | 610 ms                                                                 | 740 ms: 1.21x slower                                                     |
| async_tree_io              | 627 ms                                                                 | 761 ms: 1.21x slower                                                     |
| many_optionals             | 1.02 ms                                                                | 1.24 ms: 1.21x slower                                                    |
| nqueens                    | 80.3 ms                                                                | 97.6 ms: 1.22x slower                                                    |
| mdp                        | 2.33 sec                                                               | 2.86 sec: 1.23x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.39 sec: 1.24x slower                                                   |
| scimark_fft                | 314 ms                                                                 | 392 ms: 1.25x slower                                                     |
| coverage                   | 79.2 ms                                                                | 99.2 ms: 1.25x slower                                                    |
| connected_components       | 398 ms                                                                 | 499 ms: 1.25x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 14.2 ms: 1.25x slower                                                    |
| xml_etree_process          | 58.8 ms                                                                | 73.8 ms: 1.25x slower                                                    |
| async_tree_none_tg         | 256 ms                                                                 | 322 ms: 1.26x slower                                                     |
| shortest_path              | 438 ms                                                                 | 552 ms: 1.26x slower                                                     |
| deepcopy                   | 256 us                                                                 | 323 us: 1.26x slower                                                     |
| async_generators           | 352 ms                                                                 | 444 ms: 1.26x slower                                                     |
| sqlglot_optimize           | 52.1 ms                                                                | 65.7 ms: 1.26x slower                                                    |
| async_tree_none            | 277 ms                                                                 | 354 ms: 1.28x slower                                                     |
| genshi_xml                 | 49.7 ms                                                                | 63.7 ms: 1.28x slower                                                    |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.62 ms: 1.28x slower                                                    |
| sqlglot_normalize          | 103 ms                                                                 | 133 ms: 1.29x slower                                                     |
| async_tree_memoization     | 332 ms                                                                 | 429 ms: 1.29x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.30x slower                                                     |
| pylint                     | 280 ms                                                                 | 364 ms: 1.30x slower                                                     |
| async_tree_memoization_tg  | 307 ms                                                                 | 401 ms: 1.30x slower                                                     |
| typing_runtime_protocols   | 155 us                                                                 | 203 us: 1.31x slower                                                     |
| tomli_loads                | 1.97 sec                                                               | 2.58 sec: 1.31x slower                                                   |
| subparsers                 | 22.2 ms                                                                | 29.2 ms: 1.31x slower                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 3.42 us: 1.31x slower                                                    |
| regex_compile              | 127 ms                                                                 | 170 ms: 1.34x slower                                                     |
| fannkuch                   | 372 ms                                                                 | 498 ms: 1.34x slower                                                     |
| deepcopy_memo              | 30.1 us                                                                | 40.8 us: 1.35x slower                                                    |
| thrift                     | 738 us                                                                 | 1.00 ms: 1.36x slower                                                    |
| pprint_safe_repr           | 710 ms                                                                 | 965 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                    |
| pprint_pformat             | 1.45 sec                                                               | 2.00 sec: 1.37x slower                                                   |
| crypto_pyaes               | 65.4 ms                                                                | 90.7 ms: 1.39x slower                                                    |
| 2to3                       | 256 ms                                                                 | 360 ms: 1.41x slower                                                     |
| django_template            | 35.4 ms                                                                | 50.2 ms: 1.42x slower                                                    |
| generators                 | 27.1 ms                                                                | 38.5 ms: 1.42x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 30.9 ms: 1.43x slower                                                    |
| nbody                      | 90.3 ms                                                                | 131 ms: 1.45x slower                                                     |
| float                      | 76.4 ms                                                                | 111 ms: 1.45x slower                                                     |
| sqlalchemy_imperative      | 19.1 ms                                                                | 27.8 ms: 1.46x slower                                                    |
| logging_simple             | 6.14 us                                                                | 9.06 us: 1.48x slower                                                    |
| sympy_integrate            | 19.9 ms                                                                | 29.4 ms: 1.48x slower                                                    |
| mako                       | 11.6 ms                                                                | 17.2 ms: 1.48x slower                                                    |
| logging_format             | 6.79 us                                                                | 10.1 us: 1.49x slower                                                    |
| richards_super             | 50.7 ms                                                                | 77.6 ms: 1.53x slower                                                    |
| richards                   | 44.7 ms                                                                | 69.1 ms: 1.55x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 196 ms: 1.55x slower                                                     |
| pickle_pure_python         | 323 us                                                                 | 502 us: 1.55x slower                                                     |
| unpickle_pure_python       | 213 us                                                                 | 331 us: 1.56x slower                                                     |
| pyflate                    | 421 ms                                                                 | 662 ms: 1.57x slower                                                     |
| comprehensions             | 17.2 us                                                                | 27.7 us: 1.61x slower                                                    |
| chaos                      | 58.4 ms                                                                | 95.9 ms: 1.64x slower                                                    |
| scimark_monte_carlo        | 64.7 ms                                                                | 108 ms: 1.66x slower                                                     |
| scimark_lu                 | 110 ms                                                                 | 185 ms: 1.68x slower                                                     |
| hexiom                     | 5.84 ms                                                                | 9.87 ms: 1.69x slower                                                    |
| sqlglot_transpile          | 1.57 ms                                                                | 2.69 ms: 1.72x slower                                                    |
| sympy_str                  | 271 ms                                                                 | 473 ms: 1.75x slower                                                     |
| logging_silent             | 106 ns                                                                 | 186 ns: 1.76x slower                                                     |
| scimark_sor                | 128 ms                                                                 | 232 ms: 1.82x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                                | 2.33 ms: 1.86x slower                                                    |
| raytrace                   | 260 ms                                                                 | 495 ms: 1.90x slower                                                     |
| go                         | 117 ms                                                                 | 244 ms: 2.09x slower                                                     |
| sympy_expand               | 453 ms                                                                 | 953 ms: 2.10x slower                                                     |
| sympy_sum                  | 152 ms                                                                 | 348 ms: 2.29x slower                                                     |
| deltablue                  | 3.17 ms                                                                | 7.65 ms: 2.41x slower                                                    |
| bench_thread_pool          | 1.04 ms                                                                | 3.37 ms: 3.25x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.35x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab.json: html5lib

- Geometric mean (including insignificant results): 1.250x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x