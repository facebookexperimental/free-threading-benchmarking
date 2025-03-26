# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: aeb389d
- commit date: 2025-03-25
- overall geometric mean: 1.112x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 298 ms: 1.16x slower                                                  |
| docutils       | 2.59 sec                                                               | 2.77 sec: 1.07x slower                                                |
| sphinx         | 992 ms                                                                 | 1.10 sec: 1.11x slower                                                |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 646 ms                                                                 | 557 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 261 ms                                                                 | 237 ms: 1.10x faster                                                  |
| async_tree_io              | 632 ms                                                                 | 588 ms: 1.07x faster                                                  |
| async_tree_memoization_tg  | 311 ms                                                                 | 302 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 485 ms: 1.02x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 276 ms: 1.01x faster                                                  |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 524 ms: 1.02x slower                                                  |
| async_tree_memoization     | 321 ms                                                                 | 337 ms: 1.05x slower                                                  |
| async_generators           | 341 ms                                                                 | 387 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 74.2 ms                                                                | 76.5 ms: 1.03x slower                                                 |
| pidigits       | 193 ms                                                                 | 208 ms: 1.07x slower                                                  |
| nbody          | 101 ms                                                                 | 132 ms: 1.31x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.64 ms: 1.05x faster                                                 |
| regex_v8       | 22.2 ms                                                                | 21.6 ms: 1.03x faster                                                 |
| regex_dna      | 175 ms                                                                 | 180 ms: 1.03x slower                                                  |
| regex_compile  | 127 ms                                                                 | 158 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.9 ms                                                                | 88.4 ms: 1.05x faster                                                 |
| xml_etree_parse      | 131 ms                                                                 | 129 ms: 1.01x faster                                                  |
| json_loads           | 28.2 us                                                                | 29.4 us: 1.04x slower                                                 |
| pickle_pure_python   | 320 us                                                                 | 364 us: 1.14x slower                                                  |
| unpickle_pure_python | 221 us                                                                 | 252 us: 1.14x slower                                                  |
| xml_etree_generate   | 84.9 ms                                                                | 97.3 ms: 1.15x slower                                                 |
| json_dumps           | 11.2 ms                                                                | 13.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.4 ms                                                                | 71.1 ms: 1.20x slower                                                 |
| tomli_loads          | 1.96 sec                                                               | 2.35 sec: 1.20x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                                 |
| python_startup_no_site | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.9 ms                                                                | 59.5 ms: 1.17x slower                                                 |
| django_template | 36.1 ms                                                                | 42.4 ms: 1.18x slower                                                 |
| genshi_text     | 22.6 ms                                                                | 28.3 ms: 1.26x slower                                                 |
| mako            | 12.2 ms                                                                | 15.8 ms: 1.30x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.59 ms                                                                | 1.80 ms: 2.55x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.35 ms: 1.38x faster                                                 |
| async_tree_io_tg           | 646 ms                                                                 | 557 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 261 ms                                                                 | 237 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.04 us: 1.09x faster                                                 |
| async_tree_io              | 632 ms                                                                 | 588 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 92.9 ms                                                                | 88.4 ms: 1.05x faster                                                 |
| regex_effbot               | 2.78 ms                                                                | 2.64 ms: 1.05x faster                                                 |
| async_tree_memoization_tg  | 311 ms                                                                 | 302 ms: 1.03x faster                                                  |
| regex_v8                   | 22.2 ms                                                                | 21.6 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 485 ms: 1.02x faster                                                  |
| xml_etree_parse            | 131 ms                                                                 | 129 ms: 1.01x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 276 ms: 1.01x faster                                                  |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 524 ms: 1.02x slower                                                  |
| json                       | 4.96 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| regex_dna                  | 175 ms                                                                 | 180 ms: 1.03x slower                                                  |
| float                      | 74.2 ms                                                                | 76.5 ms: 1.03x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 20.1 ms: 1.04x slower                                                 |
| json_loads                 | 28.2 us                                                                | 29.4 us: 1.04x slower                                                 |
| pycparser                  | 1.14 sec                                                               | 1.19 sec: 1.05x slower                                                |
| async_tree_memoization     | 321 ms                                                                 | 337 ms: 1.05x slower                                                  |
| generators                 | 29.4 ms                                                                | 31.0 ms: 1.06x slower                                                 |
| python_startup             | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                                 |
| docutils                   | 2.59 sec                                                               | 2.77 sec: 1.07x slower                                                |
| pidigits                   | 193 ms                                                                 | 208 ms: 1.07x slower                                                  |
| bench_mp_pool              | 89.4 ms                                                                | 97.4 ms: 1.09x slower                                                 |
| mdp                        | 2.47 sec                                                               | 2.73 sec: 1.10x slower                                                |
| sphinx                     | 992 ms                                                                 | 1.10 sec: 1.11x slower                                                |
| dulwich_log                | 66.2 ms                                                                | 73.7 ms: 1.11x slower                                                 |
| k_core                     | 2.07 sec                                                               | 2.31 sec: 1.11x slower                                                |
| pylint                     | 283 ms                                                                 | 315 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.35 sec                                                               | 4.88 sec: 1.12x slower                                                |
| subparsers                 | 22.6 ms                                                                | 25.6 ms: 1.13x slower                                                 |
| async_generators           | 341 ms                                                                 | 387 ms: 1.13x slower                                                  |
| pickle_pure_python         | 320 us                                                                 | 364 us: 1.14x slower                                                  |
| logging_silent             | 98.6 ns                                                                | 112 ns: 1.14x slower                                                  |
| unpickle_pure_python       | 221 us                                                                 | 252 us: 1.14x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 731 ms                                                                 | 838 ms: 1.15x slower                                                  |
| xml_etree_generate         | 84.9 ms                                                                | 97.3 ms: 1.15x slower                                                 |
| deepcopy_reduce            | 2.77 us                                                                | 3.19 us: 1.15x slower                                                 |
| thrift                     | 758 us                                                                 | 876 us: 1.16x slower                                                  |
| json_dumps                 | 11.2 ms                                                                | 13.0 ms: 1.16x slower                                                 |
| 2to3                       | 256 ms                                                                 | 298 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.48 sec                                                               | 1.73 sec: 1.17x slower                                                |
| genshi_xml                 | 50.9 ms                                                                | 59.5 ms: 1.17x slower                                                 |
| django_template            | 36.1 ms                                                                | 42.4 ms: 1.18x slower                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                 | 122 ms: 1.18x slower                                                  |
| deepcopy                   | 266 us                                                                 | 313 us: 1.18x slower                                                  |
| nqueens                    | 82.9 ms                                                                | 97.6 ms: 1.18x slower                                                 |
| sqlglot_v2_optimize        | 52.2 ms                                                                | 61.5 ms: 1.18x slower                                                 |
| sympy_expand               | 465 ms                                                                 | 553 ms: 1.19x slower                                                  |
| sympy_sum                  | 156 ms                                                                 | 186 ms: 1.19x slower                                                  |
| xml_etree_process          | 59.4 ms                                                                | 71.1 ms: 1.20x slower                                                 |
| tomli_loads                | 1.96 sec                                                               | 2.35 sec: 1.20x slower                                                |
| chaos                      | 57.1 ms                                                                | 68.4 ms: 1.20x slower                                                 |
| pyflate                    | 422 ms                                                                 | 506 ms: 1.20x slower                                                  |
| scimark_sor                | 113 ms                                                                 | 136 ms: 1.20x slower                                                  |
| logging_simple             | 6.09 us                                                                | 7.34 us: 1.20x slower                                                 |
| spectral_norm              | 93.0 ms                                                                | 112 ms: 1.21x slower                                                  |
| sympy_integrate            | 19.5 ms                                                                | 23.7 ms: 1.21x slower                                                 |
| comprehensions             | 17.0 us                                                                | 20.7 us: 1.22x slower                                                 |
| sqlalchemy_declarative     | 129 ms                                                                 | 158 ms: 1.22x slower                                                  |
| raytrace                   | 263 ms                                                                 | 322 ms: 1.22x slower                                                  |
| telco                      | 7.41 ms                                                                | 9.09 ms: 1.23x slower                                                 |
| sqlglot_v2_transpile       | 1.58 ms                                                                | 1.94 ms: 1.23x slower                                                 |
| sympy_str                  | 275 ms                                                                 | 338 ms: 1.23x slower                                                  |
| scimark_fft                | 323 ms                                                                 | 397 ms: 1.23x slower                                                  |
| sqlalchemy_imperative      | 19.6 ms                                                                | 24.2 ms: 1.23x slower                                                 |
| crypto_pyaes               | 71.3 ms                                                                | 87.9 ms: 1.23x slower                                                 |
| fannkuch                   | 401 ms                                                                 | 497 ms: 1.24x slower                                                  |
| shortest_path              | 443 ms                                                                 | 550 ms: 1.24x slower                                                  |
| deltablue                  | 3.11 ms                                                                | 3.86 ms: 1.24x slower                                                 |
| regex_compile              | 127 ms                                                                 | 158 ms: 1.25x slower                                                  |
| logging_format             | 6.73 us                                                                | 8.41 us: 1.25x slower                                                 |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.60 ms: 1.25x slower                                                 |
| hexiom                     | 6.08 ms                                                                | 7.63 ms: 1.25x slower                                                 |
| genshi_text                | 22.6 ms                                                                | 28.3 ms: 1.26x slower                                                 |
| connected_components       | 398 ms                                                                 | 505 ms: 1.27x slower                                                  |
| scimark_monte_carlo        | 65.6 ms                                                                | 83.4 ms: 1.27x slower                                                 |
| meteor_contest             | 102 ms                                                                 | 130 ms: 1.27x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                  |
| go                         | 113 ms                                                                 | 144 ms: 1.28x slower                                                  |
| richards                   | 42.6 ms                                                                | 54.7 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 4.47 ms                                                                | 5.78 ms: 1.29x slower                                                 |
| python_startup_no_site     | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                                 |
| typing_runtime_protocols   | 157 us                                                                 | 203 us: 1.29x slower                                                  |
| deepcopy_memo              | 30.4 us                                                                | 39.3 us: 1.30x slower                                                 |
| mako                       | 12.2 ms                                                                | 15.8 ms: 1.30x slower                                                 |
| richards_super             | 48.4 ms                                                                | 63.4 ms: 1.31x slower                                                 |
| nbody                      | 101 ms                                                                 | 132 ms: 1.31x slower                                                  |
| coverage                   | 78.7 ms                                                                | 109 ms: 1.38x slower                                                  |
| bench_thread_pool          | 1.06 ms                                                                | 3.16 ms: 2.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250325-3.14.0a6+-aeb389d-NOGIL/bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d.json: html5lib

- Geometric mean (including insignificant results): 1.112x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x