# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.153x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 318 ms: 1.25x slower                                                 |
| docutils       | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                               |
| sphinx         | 992 ms                                                                 | 1.12 sec: 1.13x slower                                               |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg      | 258 ms                                                                 | 239 ms: 1.08x faster                                                 |
| async_tree_io_tg        | 622 ms                                                                 | 591 ms: 1.05x faster                                                 |
| async_tree_io           | 630 ms                                                                 | 604 ms: 1.04x faster                                                 |
| asyncio_websockets      | 523 ms                                                                 | 519 ms: 1.01x faster                                                 |
| async_tree_none         | 279 ms                                                                 | 283 ms: 1.02x slower                                                 |
| coroutines              | 22.7 ms                                                                | 23.1 ms: 1.02x slower                                                |
| async_tree_cpu_io_mixed | 498 ms                                                                 | 514 ms: 1.03x slower                                                 |
| async_tree_memoization  | 336 ms                                                                 | 347 ms: 1.03x slower                                                 |
| async_generators        | 354 ms                                                                 | 422 ms: 1.19x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                 |
| float          | 77.0 ms                                                                | 83.0 ms: 1.08x slower                                                |
| nbody          | 91.2 ms                                                                | 133 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 24.0 ms: 1.02x slower                                                |
| regex_dna      | 167 ms                                                                 | 176 ms: 1.06x slower                                                 |
| regex_effbot   | 2.70 ms                                                                | 2.86 ms: 1.06x slower                                                |
| regex_compile  | 126 ms                                                                 | 151 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.9 ms                                                                | 88.1 ms: 1.03x faster                                                |
| xml_etree_parse      | 128 ms                                                                 | 131 ms: 1.02x slower                                                 |
| json_loads           | 25.9 us                                                                | 27.8 us: 1.07x slower                                                |
| pickle_pure_python   | 322 us                                                                 | 365 us: 1.13x slower                                                 |
| xml_etree_generate   | 83.7 ms                                                                | 96.4 ms: 1.15x slower                                                |
| json_dumps           | 11.5 ms                                                                | 13.2 ms: 1.15x slower                                                |
| unpickle_pure_python | 212 us                                                                 | 248 us: 1.17x slower                                                 |
| xml_etree_process    | 58.3 ms                                                                | 68.6 ms: 1.18x slower                                                |
| tomli_loads          | 1.97 sec                                                               | 2.34 sec: 1.19x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.0 ms: 1.17x slower                                                |
| python_startup_no_site | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.4 ms                                                                | 59.6 ms: 1.21x slower                                                |
| django_template | 35.4 ms                                                                | 43.4 ms: 1.23x slower                                                |
| genshi_text     | 21.5 ms                                                                | 28.1 ms: 1.31x slower                                                |
| mako            | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 4.59 ms                                                                | 3.29 ms: 1.40x faster                                                |
| sqlite_synth             | 2.25 us                                                                | 2.04 us: 1.10x faster                                                |
| async_tree_none_tg       | 258 ms                                                                 | 239 ms: 1.08x faster                                                 |
| async_tree_io_tg         | 622 ms                                                                 | 591 ms: 1.05x faster                                                 |
| async_tree_io            | 630 ms                                                                 | 604 ms: 1.04x faster                                                 |
| xml_etree_iterparse      | 90.9 ms                                                                | 88.1 ms: 1.03x faster                                                |
| pidigits                 | 185 ms                                                                 | 181 ms: 1.02x faster                                                 |
| create_gc_cycles         | 1.84 ms                                                                | 1.80 ms: 1.02x faster                                                |
| asyncio_websockets       | 523 ms                                                                 | 519 ms: 1.01x faster                                                 |
| async_tree_none          | 279 ms                                                                 | 283 ms: 1.02x slower                                                 |
| regex_v8                 | 23.5 ms                                                                | 24.0 ms: 1.02x slower                                                |
| coroutines               | 22.7 ms                                                                | 23.1 ms: 1.02x slower                                                |
| xml_etree_parse          | 128 ms                                                                 | 131 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed  | 498 ms                                                                 | 514 ms: 1.03x slower                                                 |
| async_tree_memoization   | 336 ms                                                                 | 347 ms: 1.03x slower                                                 |
| pathlib                  | 18.2 ms                                                                | 18.9 ms: 1.04x slower                                                |
| json                     | 4.74 ms                                                                | 4.94 ms: 1.04x slower                                                |
| regex_dna                | 167 ms                                                                 | 176 ms: 1.06x slower                                                 |
| regex_effbot             | 2.70 ms                                                                | 2.86 ms: 1.06x slower                                                |
| json_loads               | 25.9 us                                                                | 27.8 us: 1.07x slower                                                |
| float                    | 77.0 ms                                                                | 83.0 ms: 1.08x slower                                                |
| dulwich_log              | 75.4 ms                                                                | 82.2 ms: 1.09x slower                                                |
| spectral_norm            | 99.1 ms                                                                | 108 ms: 1.09x slower                                                 |
| logging_silent           | 107 ns                                                                 | 117 ns: 1.09x slower                                                 |
| pycparser                | 1.11 sec                                                               | 1.22 sec: 1.10x slower                                               |
| docutils                 | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                               |
| bpe_tokeniser            | 4.26 sec                                                               | 4.74 sec: 1.11x slower                                               |
| sphinx                   | 992 ms                                                                 | 1.12 sec: 1.13x slower                                               |
| k_core                   | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                               |
| pickle_pure_python       | 322 us                                                                 | 365 us: 1.13x slower                                                 |
| subparsers               | 22.4 ms                                                                | 25.5 ms: 1.14x slower                                                |
| pyflate                  | 434 ms                                                                 | 498 ms: 1.15x slower                                                 |
| xml_etree_generate       | 83.7 ms                                                                | 96.4 ms: 1.15x slower                                                |
| many_optionals           | 1.02 ms                                                                | 1.18 ms: 1.15x slower                                                |
| json_dumps               | 11.5 ms                                                                | 13.2 ms: 1.15x slower                                                |
| python_startup           | 14.6 ms                                                                | 17.0 ms: 1.17x slower                                                |
| telco                    | 7.26 ms                                                                | 8.46 ms: 1.17x slower                                                |
| generators               | 27.1 ms                                                                | 31.6 ms: 1.17x slower                                                |
| unpickle_pure_python     | 212 us                                                                 | 248 us: 1.17x slower                                                 |
| sqlglot_normalize        | 103 ms                                                                 | 122 ms: 1.18x slower                                                 |
| xml_etree_process        | 58.3 ms                                                                | 68.6 ms: 1.18x slower                                                |
| sqlglot_optimize         | 52.0 ms                                                                | 61.2 ms: 1.18x slower                                                |
| scimark_fft              | 315 ms                                                                 | 371 ms: 1.18x slower                                                 |
| logging_simple           | 6.16 us                                                                | 7.29 us: 1.18x slower                                                |
| mdp                      | 2.34 sec                                                               | 2.76 sec: 1.18x slower                                               |
| tomli_loads              | 1.97 sec                                                               | 2.34 sec: 1.19x slower                                               |
| bench_mp_pool            | 88.5 ms                                                                | 105 ms: 1.19x slower                                                 |
| async_generators         | 354 ms                                                                 | 422 ms: 1.19x slower                                                 |
| scimark_sor              | 125 ms                                                                 | 149 ms: 1.19x slower                                                 |
| regex_compile            | 126 ms                                                                 | 151 ms: 1.19x slower                                                 |
| logging_format           | 6.91 us                                                                | 8.27 us: 1.20x slower                                                |
| pprint_safe_repr         | 713 ms                                                                 | 854 ms: 1.20x slower                                                 |
| genshi_xml               | 49.4 ms                                                                | 59.6 ms: 1.21x slower                                                |
| go                       | 118 ms                                                                 | 142 ms: 1.21x slower                                                 |
| pprint_pformat           | 1.45 sec                                                               | 1.76 sec: 1.22x slower                                               |
| chaos                    | 58.5 ms                                                                | 71.2 ms: 1.22x slower                                                |
| sqlglot_transpile        | 1.59 ms                                                                | 1.94 ms: 1.22x slower                                                |
| django_template          | 35.4 ms                                                                | 43.4 ms: 1.23x slower                                                |
| pylint                   | 280 ms                                                                 | 343 ms: 1.23x slower                                                 |
| connected_components     | 399 ms                                                                 | 492 ms: 1.23x slower                                                 |
| deepcopy                 | 255 us                                                                 | 315 us: 1.23x slower                                                 |
| thrift                   | 740 us                                                                 | 915 us: 1.24x slower                                                 |
| nqueens                  | 77.9 ms                                                                | 96.5 ms: 1.24x slower                                                |
| shortest_path            | 439 ms                                                                 | 546 ms: 1.24x slower                                                 |
| coverage                 | 79.2 ms                                                                | 98.7 ms: 1.25x slower                                                |
| 2to3                     | 255 ms                                                                 | 318 ms: 1.25x slower                                                 |
| deepcopy_reduce          | 2.61 us                                                                | 3.28 us: 1.26x slower                                                |
| richards                 | 45.1 ms                                                                | 56.8 ms: 1.26x slower                                                |
| comprehensions           | 17.0 us                                                                | 21.5 us: 1.26x slower                                                |
| sqlglot_parse            | 1.28 ms                                                                | 1.62 ms: 1.27x slower                                                |
| raytrace                 | 262 ms                                                                 | 331 ms: 1.27x slower                                                 |
| crypto_pyaes             | 68.1 ms                                                                | 86.4 ms: 1.27x slower                                                |
| scimark_monte_carlo      | 63.6 ms                                                                | 81.2 ms: 1.28x slower                                                |
| sqlalchemy_imperative    | 19.0 ms                                                                | 24.3 ms: 1.28x slower                                                |
| scimark_sparse_mat_mult  | 4.15 ms                                                                | 5.31 ms: 1.28x slower                                                |
| typing_runtime_protocols | 155 us                                                                 | 200 us: 1.29x slower                                                 |
| hexiom                   | 5.91 ms                                                                | 7.65 ms: 1.30x slower                                                |
| richards_super           | 50.9 ms                                                                | 66.1 ms: 1.30x slower                                                |
| meteor_contest           | 99.9 ms                                                                | 130 ms: 1.30x slower                                                 |
| deepcopy_memo            | 29.9 us                                                                | 39.0 us: 1.30x slower                                                |
| genshi_text              | 21.5 ms                                                                | 28.1 ms: 1.31x slower                                                |
| fannkuch                 | 367 ms                                                                 | 480 ms: 1.31x slower                                                 |
| mako                     | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                |
| python_startup_no_site   | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                |
| sqlalchemy_declarative   | 126 ms                                                                 | 177 ms: 1.40x slower                                                 |
| sympy_integrate          | 19.7 ms                                                                | 28.4 ms: 1.44x slower                                                |
| scimark_lu               | 110 ms                                                                 | 161 ms: 1.46x slower                                                 |
| nbody                    | 91.2 ms                                                                | 133 ms: 1.46x slower                                                 |
| deltablue                | 3.23 ms                                                                | 4.72 ms: 1.46x slower                                                |
| sympy_str                | 270 ms                                                                 | 458 ms: 1.70x slower                                                 |
| sympy_expand             | 456 ms                                                                 | 927 ms: 2.03x slower                                                 |
| sympy_sum                | 152 ms                                                                 | 340 ms: 2.25x slower                                                 |
| bench_thread_pool        | 1.03 ms                                                                | 3.33 ms: 3.23x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.19x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: html5lib

- Geometric mean (including insignificant results): 1.153x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x