# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: 33deca3
- commit date: 2025-01-03
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 351 ms                                                                 | 312 ms: 1.12x faster                                                 |
| docutils       | 3.00 sec                                                               | 2.84 sec: 1.06x faster                                               |
| html5lib       | 93.1 ms                                                                | 72.9 ms: 1.28x faster                                                |
| sphinx         | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                               |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 306 ms                                                                 | 234 ms: 1.31x faster                                                 |
| async_tree_memoization_tg  | 389 ms                                                                 | 306 ms: 1.27x faster                                                 |
| async_tree_io              | 744 ms                                                                 | 600 ms: 1.24x faster                                                 |
| async_tree_none            | 343 ms                                                                 | 278 ms: 1.23x faster                                                 |
| async_tree_io_tg           | 721 ms                                                                 | 587 ms: 1.23x faster                                                 |
| async_tree_memoization     | 421 ms                                                                 | 344 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                 | 478 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed    | 583 ms                                                                 | 512 ms: 1.14x faster                                                 |
| async_generators           | 450 ms                                                                 | 419 ms: 1.07x faster                                                 |
| coroutines                 | 24.7 ms                                                                | 23.2 ms: 1.07x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.17x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 111 ms                                                                 | 79.1 ms: 1.41x faster                                                |
| pidigits       | 194 ms                                                                 | 191 ms: 1.01x faster                                                 |
| nbody          | 130 ms                                                                 | 132 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 168 ms                                                                 | 151 ms: 1.12x faster                                                 |
| regex_effbot   | 2.80 ms                                                                | 2.72 ms: 1.03x faster                                                |
| regex_dna      | 182 ms                                                                 | 179 ms: 1.02x faster                                                 |
| regex_v8       | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 499 us                                                                 | 373 us: 1.34x faster                                                 |
| unpickle_pure_python | 325 us                                                                 | 249 us: 1.31x faster                                                 |
| tomli_loads          | 2.52 sec                                                               | 2.33 sec: 1.08x faster                                               |
| xml_etree_process    | 74.5 ms                                                                | 69.0 ms: 1.08x faster                                                |
| json_dumps           | 13.7 ms                                                                | 13.0 ms: 1.05x faster                                                |
| xml_etree_iterparse  | 89.6 ms                                                                | 87.9 ms: 1.02x faster                                                |
| json_loads           | 27.9 us                                                                | 27.5 us: 1.01x faster                                                |
| xml_etree_generate   | 98.0 ms                                                                | 96.9 ms: 1.01x faster                                                |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                |
| python_startup_no_site | 9.81 ms                                                                | 9.71 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 49.6 ms                                                                | 43.5 ms: 1.14x faster                                                |
| mako            | 17.3 ms                                                                | 15.8 ms: 1.10x faster                                                |
| genshi_text     | 30.2 ms                                                                | 28.5 ms: 1.06x faster                                                |
| genshi_xml      | 62.3 ms                                                                | 61.2 ms: 1.02x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.08x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| go                         | 237 ms                                                                 | 140 ms: 1.69x faster                                                 |
| scimark_sor                | 215 ms                                                                 | 136 ms: 1.58x faster                                                 |
| deltablue                  | 7.45 ms                                                                | 4.80 ms: 1.55x faster                                                |
| logging_silent             | 179 ns                                                                 | 117 ns: 1.53x faster                                                 |
| sqlglot_parse              | 2.38 ms                                                                | 1.60 ms: 1.48x faster                                                |
| raytrace                   | 485 ms                                                                 | 331 ms: 1.46x faster                                                 |
| sqlglot_transpile          | 2.74 ms                                                                | 1.94 ms: 1.41x faster                                                |
| float                      | 111 ms                                                                 | 79.1 ms: 1.41x faster                                                |
| pyflate                    | 660 ms                                                                 | 488 ms: 1.35x faster                                                 |
| pickle_pure_python         | 499 us                                                                 | 373 us: 1.34x faster                                                 |
| chaos                      | 93.8 ms                                                                | 71.3 ms: 1.32x faster                                                |
| async_tree_none_tg         | 306 ms                                                                 | 234 ms: 1.31x faster                                                 |
| unpickle_pure_python       | 325 us                                                                 | 249 us: 1.31x faster                                                 |
| comprehensions             | 27.2 us                                                                | 21.0 us: 1.29x faster                                                |
| scimark_monte_carlo        | 105 ms                                                                 | 82.3 ms: 1.28x faster                                                |
| html5lib                   | 93.1 ms                                                                | 72.9 ms: 1.28x faster                                                |
| hexiom                     | 9.58 ms                                                                | 7.51 ms: 1.28x faster                                                |
| async_tree_memoization_tg  | 389 ms                                                                 | 306 ms: 1.27x faster                                                 |
| async_tree_io              | 744 ms                                                                 | 600 ms: 1.24x faster                                                 |
| async_tree_none            | 343 ms                                                                 | 278 ms: 1.23x faster                                                 |
| async_tree_io_tg           | 721 ms                                                                 | 587 ms: 1.23x faster                                                 |
| logging_simple             | 9.00 us                                                                | 7.35 us: 1.22x faster                                                |
| async_tree_memoization     | 421 ms                                                                 | 344 ms: 1.22x faster                                                 |
| logging_format             | 10.1 us                                                                | 8.29 us: 1.22x faster                                                |
| generators                 | 37.8 ms                                                                | 31.6 ms: 1.20x faster                                                |
| richards                   | 67.1 ms                                                                | 56.0 ms: 1.20x faster                                                |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                 | 478 ms: 1.16x faster                                                 |
| pprint_pformat             | 1.97 sec                                                               | 1.70 sec: 1.16x faster                                               |
| pprint_safe_repr           | 946 ms                                                                 | 819 ms: 1.15x faster                                                 |
| django_template            | 49.6 ms                                                                | 43.5 ms: 1.14x faster                                                |
| async_tree_cpu_io_mixed    | 583 ms                                                                 | 512 ms: 1.14x faster                                                 |
| richards_super             | 74.4 ms                                                                | 65.4 ms: 1.14x faster                                                |
| pycparser                  | 1.36 sec                                                               | 1.21 sec: 1.13x faster                                               |
| sqlalchemy_imperative      | 27.7 ms                                                                | 24.7 ms: 1.12x faster                                                |
| 2to3                       | 351 ms                                                                 | 312 ms: 1.12x faster                                                 |
| subparsers                 | 28.7 ms                                                                | 25.7 ms: 1.12x faster                                                |
| regex_compile              | 168 ms                                                                 | 151 ms: 1.12x faster                                                 |
| sqlalchemy_declarative     | 181 ms                                                                 | 163 ms: 1.11x faster                                                 |
| dulwich_log                | 90.6 ms                                                                | 81.8 ms: 1.11x faster                                                |
| scimark_lu                 | 157 ms                                                                 | 142 ms: 1.11x faster                                                 |
| mdp                        | 2.86 sec                                                               | 2.60 sec: 1.10x faster                                               |
| sqlglot_normalize          | 134 ms                                                                 | 122 ms: 1.10x faster                                                 |
| mako                       | 17.3 ms                                                                | 15.8 ms: 1.10x faster                                                |
| tomli_loads                | 2.52 sec                                                               | 2.33 sec: 1.08x faster                                               |
| xml_etree_process          | 74.5 ms                                                                | 69.0 ms: 1.08x faster                                                |
| sqlglot_optimize           | 67.1 ms                                                                | 62.5 ms: 1.07x faster                                                |
| async_generators           | 450 ms                                                                 | 419 ms: 1.07x faster                                                 |
| thrift                     | 994 us                                                                 | 926 us: 1.07x faster                                                 |
| coroutines                 | 24.7 ms                                                                | 23.2 ms: 1.07x faster                                                |
| gc_traversal               | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                |
| pathlib                    | 19.9 ms                                                                | 18.7 ms: 1.06x faster                                                |
| spectral_norm              | 117 ms                                                                 | 110 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 5.05 sec                                                               | 4.76 sec: 1.06x faster                                               |
| genshi_text                | 30.2 ms                                                                | 28.5 ms: 1.06x faster                                                |
| pylint                     | 345 ms                                                                 | 326 ms: 1.06x faster                                                 |
| many_optionals             | 1.24 ms                                                                | 1.17 ms: 1.06x faster                                                |
| sympy_expand               | 585 ms                                                                 | 554 ms: 1.06x faster                                                 |
| docutils                   | 3.00 sec                                                               | 2.84 sec: 1.06x faster                                               |
| sympy_str                  | 355 ms                                                                 | 336 ms: 1.05x faster                                                 |
| json_dumps                 | 13.7 ms                                                                | 13.0 ms: 1.05x faster                                                |
| sympy_sum                  | 194 ms                                                                 | 186 ms: 1.05x faster                                                 |
| scimark_fft                | 400 ms                                                                 | 382 ms: 1.05x faster                                                 |
| fannkuch                   | 501 ms                                                                 | 480 ms: 1.04x faster                                                 |
| meteor_contest             | 133 ms                                                                 | 128 ms: 1.04x faster                                                 |
| crypto_pyaes               | 90.3 ms                                                                | 86.7 ms: 1.04x faster                                                |
| sympy_integrate            | 25.3 ms                                                                | 24.3 ms: 1.04x faster                                                |
| deepcopy_memo              | 40.2 us                                                                | 38.7 us: 1.04x faster                                                |
| nqueens                    | 101 ms                                                                 | 97.6 ms: 1.04x faster                                                |
| sphinx                     | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                               |
| bench_mp_pool              | 100 ms                                                                 | 97.8 ms: 1.03x faster                                                |
| sqlite_synth               | 2.12 us                                                                | 2.06 us: 1.03x faster                                                |
| regex_effbot               | 2.80 ms                                                                | 2.72 ms: 1.03x faster                                                |
| typing_runtime_protocols   | 204 us                                                                 | 199 us: 1.03x faster                                                 |
| create_gc_cycles           | 1.84 ms                                                                | 1.80 ms: 1.02x faster                                                |
| connected_components       | 501 ms                                                                 | 491 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.79 ms                                                                | 5.67 ms: 1.02x faster                                                |
| xml_etree_iterparse        | 89.6 ms                                                                | 87.9 ms: 1.02x faster                                                |
| genshi_xml                 | 62.3 ms                                                                | 61.2 ms: 1.02x faster                                                |
| regex_dna                  | 182 ms                                                                 | 179 ms: 1.02x faster                                                 |
| shortest_path              | 550 ms                                                                 | 541 ms: 1.02x faster                                                 |
| k_core                     | 2.35 sec                                                               | 2.31 sec: 1.02x faster                                               |
| deepcopy_reduce            | 3.39 us                                                                | 3.34 us: 1.02x faster                                                |
| deepcopy                   | 323 us                                                                 | 318 us: 1.02x faster                                                 |
| bench_thread_pool          | 3.39 ms                                                                | 3.34 ms: 1.02x faster                                                |
| json                       | 4.91 ms                                                                | 4.84 ms: 1.02x faster                                                |
| python_startup             | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                |
| coverage                   | 100 ms                                                                 | 98.8 ms: 1.01x faster                                                |
| json_loads                 | 27.9 us                                                                | 27.5 us: 1.01x faster                                                |
| pidigits                   | 194 ms                                                                 | 191 ms: 1.01x faster                                                 |
| xml_etree_generate         | 98.0 ms                                                                | 96.9 ms: 1.01x faster                                                |
| python_startup_no_site     | 9.81 ms                                                                | 9.71 ms: 1.01x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                 |
| nbody                      | 130 ms                                                                 | 132 ms: 1.01x slower                                                 |
| regex_v8                   | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                |
| telco                      | 8.54 ms                                                                | 8.73 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.01x