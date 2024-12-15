# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.150x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 582 ms                                                                 | 531 ms: 1.09x faster                                                 |
| docutils       | 4.39 sec                                                               | 4.14 sec: 1.06x faster                                               |
| html5lib       | 128 ms                                                                 | 101 ms: 1.26x faster                                                 |
| sphinx         | 1.68 sec                                                               | 1.63 sec: 1.03x faster                                               |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 448 ms                                                                 | 315 ms: 1.42x faster                                                 |
| async_tree_io_tg           | 1.03 sec                                                               | 764 ms: 1.35x faster                                                 |
| async_tree_memoization_tg  | 623 ms                                                                 | 462 ms: 1.35x faster                                                 |
| async_tree_none            | 533 ms                                                                 | 406 ms: 1.31x faster                                                 |
| async_tree_io              | 1.07 sec                                                               | 828 ms: 1.29x faster                                                 |
| async_tree_memoization     | 681 ms                                                                 | 536 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 803 ms                                                                 | 637 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 851 ms                                                                 | 718 ms: 1.19x faster                                                 |
| async_generators           | 677 ms                                                                 | 600 ms: 1.13x faster                                                 |
| coroutines                 | 34.7 ms                                                                | 31.9 ms: 1.09x faster                                                |
| asyncio_websockets         | 763 ms                                                                 | 730 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 159 ms                                                                 | 110 ms: 1.45x faster                                                 |
| nbody          | 182 ms                                                                 | 174 ms: 1.04x faster                                                 |
| pidigits       | 234 ms                                                                 | 243 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 36.2 ms                                                                | 32.5 ms: 1.11x faster                                                |
| regex_compile  | 222 ms                                                                 | 209 ms: 1.06x faster                                                 |
| regex_effbot   | 4.34 ms                                                                | 4.15 ms: 1.05x faster                                                |
| regex_dna      | 290 ms                                                                 | 279 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 430 us                                                                 | 328 us: 1.31x faster                                                 |
| pickle_pure_python   | 605 us                                                                 | 486 us: 1.24x faster                                                 |
| json_dumps           | 18.6 ms                                                                | 16.9 ms: 1.10x faster                                                |
| tomli_loads          | 3.30 sec                                                               | 3.02 sec: 1.09x faster                                               |
| xml_etree_iterparse  | 145 ms                                                                 | 135 ms: 1.07x faster                                                 |
| json_loads           | 38.8 us                                                                | 36.6 us: 1.06x faster                                                |
| xml_etree_process    | 103 ms                                                                 | 97.6 ms: 1.05x faster                                                |
| Geometric mean       | (ref)                                                                  | 1.11x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 34.2 ms                                                                | 31.4 ms: 1.09x faster                                                |
| python_startup_no_site | 21.0 ms                                                                | 19.9 ms: 1.05x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.07x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 63.6 ms                                                                | 51.7 ms: 1.23x faster                                                |
| genshi_xml      | 93.1 ms                                                                | 81.5 ms: 1.14x faster                                                |
| mako            | 25.7 ms                                                                | 23.7 ms: 1.08x faster                                                |
| genshi_text     | 38.6 ms                                                                | 36.3 ms: 1.06x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.13x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deltablue                  | 11.1 ms                                                                | 6.28 ms: 1.77x faster                                                |
| go                         | 314 ms                                                                 | 185 ms: 1.70x faster                                                 |
| logging_silent             | 233 ns                                                                 | 149 ns: 1.56x faster                                                 |
| scimark_sor                | 290 ms                                                                 | 186 ms: 1.56x faster                                                 |
| raytrace                   | 646 ms                                                                 | 435 ms: 1.49x faster                                                 |
| sqlglot_parse              | 3.30 ms                                                                | 2.27 ms: 1.45x faster                                                |
| float                      | 159 ms                                                                 | 110 ms: 1.45x faster                                                 |
| async_tree_none_tg         | 448 ms                                                                 | 315 ms: 1.42x faster                                                 |
| sqlglot_transpile          | 3.76 ms                                                                | 2.66 ms: 1.41x faster                                                |
| comprehensions             | 37.2 us                                                                | 26.4 us: 1.41x faster                                                |
| chaos                      | 147 ms                                                                 | 105 ms: 1.40x faster                                                 |
| logging_simple             | 12.7 us                                                                | 9.14 us: 1.39x faster                                                |
| async_tree_io_tg           | 1.03 sec                                                               | 764 ms: 1.35x faster                                                 |
| async_tree_memoization_tg  | 623 ms                                                                 | 462 ms: 1.35x faster                                                 |
| bench_thread_pool          | 4.84 ms                                                                | 3.63 ms: 1.33x faster                                                |
| async_tree_none            | 533 ms                                                                 | 406 ms: 1.31x faster                                                 |
| unpickle_pure_python       | 430 us                                                                 | 328 us: 1.31x faster                                                 |
| pyflate                    | 961 ms                                                                 | 735 ms: 1.31x faster                                                 |
| async_tree_io              | 1.07 sec                                                               | 828 ms: 1.29x faster                                                 |
| hexiom                     | 13.1 ms                                                                | 10.2 ms: 1.28x faster                                                |
| richards                   | 91.4 ms                                                                | 71.8 ms: 1.27x faster                                                |
| scimark_monte_carlo        | 139 ms                                                                 | 110 ms: 1.27x faster                                                 |
| async_tree_memoization     | 681 ms                                                                 | 536 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 803 ms                                                                 | 637 ms: 1.26x faster                                                 |
| html5lib                   | 128 ms                                                                 | 101 ms: 1.26x faster                                                 |
| logging_format             | 13.7 us                                                                | 11.0 us: 1.25x faster                                                |
| pickle_pure_python         | 605 us                                                                 | 486 us: 1.24x faster                                                 |
| create_gc_cycles           | 4.04 ms                                                                | 3.26 ms: 1.24x faster                                                |
| django_template            | 63.6 ms                                                                | 51.7 ms: 1.23x faster                                                |
| generators                 | 51.8 ms                                                                | 42.5 ms: 1.22x faster                                                |
| bench_mp_pool              | 108 ms                                                                 | 88.8 ms: 1.21x faster                                                |
| richards_super             | 103 ms                                                                 | 85.5 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 851 ms                                                                 | 718 ms: 1.19x faster                                                 |
| pprint_pformat             | 2.68 sec                                                               | 2.31 sec: 1.16x faster                                               |
| dulwich_log                | 123 ms                                                                 | 107 ms: 1.15x faster                                                 |
| pprint_safe_repr           | 1.30 sec                                                               | 1.13 sec: 1.15x faster                                               |
| pycparser                  | 1.95 sec                                                               | 1.70 sec: 1.15x faster                                               |
| sqlglot_optimize           | 91.7 ms                                                                | 80.2 ms: 1.14x faster                                                |
| genshi_xml                 | 93.1 ms                                                                | 81.5 ms: 1.14x faster                                                |
| sqlalchemy_imperative      | 37.5 ms                                                                | 32.9 ms: 1.14x faster                                                |
| bpe_tokeniser              | 8.29 sec                                                               | 7.32 sec: 1.13x faster                                               |
| async_generators           | 677 ms                                                                 | 600 ms: 1.13x faster                                                 |
| json                       | 7.60 ms                                                                | 6.80 ms: 1.12x faster                                                |
| pathlib                    | 31.7 ms                                                                | 28.4 ms: 1.12x faster                                                |
| regex_v8                   | 36.2 ms                                                                | 32.5 ms: 1.11x faster                                                |
| coverage                   | 141 ms                                                                 | 126 ms: 1.11x faster                                                 |
| sqlalchemy_declarative     | 267 ms                                                                 | 240 ms: 1.11x faster                                                 |
| mdp                        | 4.57 sec                                                               | 4.13 sec: 1.11x faster                                               |
| scimark_lu                 | 223 ms                                                                 | 203 ms: 1.10x faster                                                 |
| json_dumps                 | 18.6 ms                                                                | 16.9 ms: 1.10x faster                                                |
| 2to3                       | 582 ms                                                                 | 531 ms: 1.09x faster                                                 |
| gc_traversal               | 7.40 ms                                                                | 6.76 ms: 1.09x faster                                                |
| pylint                     | 533 ms                                                                 | 487 ms: 1.09x faster                                                 |
| tomli_loads                | 3.30 sec                                                               | 3.02 sec: 1.09x faster                                               |
| python_startup             | 34.2 ms                                                                | 31.4 ms: 1.09x faster                                                |
| coroutines                 | 34.7 ms                                                                | 31.9 ms: 1.09x faster                                                |
| mako                       | 25.7 ms                                                                | 23.7 ms: 1.08x faster                                                |
| nqueens                    | 136 ms                                                                 | 125 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 4.56 us                                                                | 4.24 us: 1.08x faster                                                |
| xml_etree_iterparse        | 145 ms                                                                 | 135 ms: 1.07x faster                                                 |
| subparsers                 | 40.4 ms                                                                | 37.6 ms: 1.07x faster                                                |
| sqlglot_normalize          | 165 ms                                                                 | 156 ms: 1.06x faster                                                 |
| genshi_text                | 38.6 ms                                                                | 36.3 ms: 1.06x faster                                                |
| shortest_path              | 1.06 sec                                                               | 997 ms: 1.06x faster                                                 |
| json_loads                 | 38.8 us                                                                | 36.6 us: 1.06x faster                                                |
| spectral_norm              | 163 ms                                                                 | 153 ms: 1.06x faster                                                 |
| regex_compile              | 222 ms                                                                 | 209 ms: 1.06x faster                                                 |
| docutils                   | 4.39 sec                                                               | 4.14 sec: 1.06x faster                                               |
| python_startup_no_site     | 21.0 ms                                                                | 19.9 ms: 1.05x faster                                                |
| xml_etree_process          | 103 ms                                                                 | 97.6 ms: 1.05x faster                                                |
| meteor_contest             | 176 ms                                                                 | 167 ms: 1.05x faster                                                 |
| sympy_expand               | 1.13 sec                                                               | 1.08 sec: 1.05x faster                                               |
| sympy_integrate            | 39.7 ms                                                                | 38.0 ms: 1.05x faster                                                |
| regex_effbot               | 4.34 ms                                                                | 4.15 ms: 1.05x faster                                                |
| k_core                     | 4.47 sec                                                               | 4.27 sec: 1.05x faster                                               |
| asyncio_websockets         | 763 ms                                                                 | 730 ms: 1.05x faster                                                 |
| thrift                     | 1.39 ms                                                                | 1.33 ms: 1.05x faster                                                |
| connected_components       | 960 ms                                                                 | 919 ms: 1.04x faster                                                 |
| nbody                      | 182 ms                                                                 | 174 ms: 1.04x faster                                                 |
| regex_dna                  | 290 ms                                                                 | 279 ms: 1.04x faster                                                 |
| sympy_sum                  | 410 ms                                                                 | 395 ms: 1.04x faster                                                 |
| sphinx                     | 1.68 sec                                                               | 1.63 sec: 1.03x faster                                               |
| pidigits                   | 234 ms                                                                 | 243 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.16x faster                                                         |

Benchmark hidden because not significant (13): xml_etree_parse, sqlite_synth, deepcopy_memo, telco, crypto_pyaes, sympy_str, fannkuch, deepcopy, xml_etree_generate, scimark_fft, scimark_sparse_mat_mult, many_optionals, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.150x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.01x