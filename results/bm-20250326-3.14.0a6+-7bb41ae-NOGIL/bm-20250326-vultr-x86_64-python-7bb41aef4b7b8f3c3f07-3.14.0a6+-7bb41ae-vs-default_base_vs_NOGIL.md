# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 7bb41aef4b7b8f3c3f07
- machine: linux-x86_64
- commit hash: 7bb41ae
- commit date: 2025-03-26
- overall geometric mean: 1.111x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 298 ms: 1.16x slower                                                   |
| docutils       | 2.59 sec                                                               | 2.78 sec: 1.07x slower                                                 |
| sphinx         | 992 ms                                                                 | 1.10 sec: 1.11x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 646 ms                                                                 | 550 ms: 1.18x faster                                                   |
| async_tree_none_tg         | 261 ms                                                                 | 237 ms: 1.10x faster                                                   |
| async_tree_io              | 632 ms                                                                 | 583 ms: 1.08x faster                                                   |
| async_tree_memoization_tg  | 311 ms                                                                 | 298 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 487 ms: 1.01x faster                                                   |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                   |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 520 ms: 1.02x slower                                                   |
| async_tree_memoization     | 321 ms                                                                 | 333 ms: 1.04x slower                                                   |
| async_generators           | 341 ms                                                                 | 388 ms: 1.14x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 196 ms: 1.01x slower                                                   |
| float          | 74.2 ms                                                                | 78.2 ms: 1.05x slower                                                  |
| nbody          | 101 ms                                                                 | 139 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                | 21.5 ms: 1.03x faster                                                  |
| regex_dna      | 175 ms                                                                 | 175 ms: 1.00x slower                                                   |
| regex_effbot   | 2.78 ms                                                                | 2.85 ms: 1.03x slower                                                  |
| regex_compile  | 127 ms                                                                 | 156 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.9 ms                                                                | 87.7 ms: 1.06x faster                                                  |
| xml_etree_parse      | 131 ms                                                                 | 129 ms: 1.01x faster                                                   |
| json_loads           | 28.2 us                                                                | 29.6 us: 1.05x slower                                                  |
| pickle_pure_python   | 320 us                                                                 | 357 us: 1.12x slower                                                   |
| xml_etree_generate   | 84.9 ms                                                                | 97.5 ms: 1.15x slower                                                  |
| json_dumps           | 11.2 ms                                                                | 12.9 ms: 1.15x slower                                                  |
| unpickle_pure_python | 221 us                                                                 | 257 us: 1.16x slower                                                   |
| tomli_loads          | 1.96 sec                                                               | 2.34 sec: 1.19x slower                                                 |
| xml_etree_process    | 59.4 ms                                                                | 70.9 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                  |
| python_startup_no_site | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                | 42.7 ms: 1.18x slower                                                  |
| genshi_xml      | 50.9 ms                                                                | 60.4 ms: 1.19x slower                                                  |
| genshi_text     | 22.6 ms                                                                | 28.4 ms: 1.26x slower                                                  |
| mako            | 12.2 ms                                                                | 15.7 ms: 1.29x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 4.59 ms                                                                | 1.80 ms: 2.56x faster                                                  |
| create_gc_cycles           | 1.86 ms                                                                | 1.36 ms: 1.37x faster                                                  |
| async_tree_io_tg           | 646 ms                                                                 | 550 ms: 1.18x faster                                                   |
| async_tree_none_tg         | 261 ms                                                                 | 237 ms: 1.10x faster                                                   |
| sqlite_synth               | 2.21 us                                                                | 2.01 us: 1.10x faster                                                  |
| async_tree_io              | 632 ms                                                                 | 583 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 92.9 ms                                                                | 87.7 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 311 ms                                                                 | 298 ms: 1.04x faster                                                   |
| regex_v8                   | 22.2 ms                                                                | 21.5 ms: 1.03x faster                                                  |
| xml_etree_parse            | 131 ms                                                                 | 129 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 487 ms: 1.01x faster                                                   |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                   |
| regex_dna                  | 175 ms                                                                 | 175 ms: 1.00x slower                                                   |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| pidigits                   | 193 ms                                                                 | 196 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 520 ms: 1.02x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.02x slower                                                  |
| regex_effbot               | 2.78 ms                                                                | 2.85 ms: 1.03x slower                                                  |
| json                       | 4.96 ms                                                                | 5.10 ms: 1.03x slower                                                  |
| async_tree_memoization     | 321 ms                                                                 | 333 ms: 1.04x slower                                                   |
| pycparser                  | 1.14 sec                                                               | 1.18 sec: 1.04x slower                                                 |
| json_loads                 | 28.2 us                                                                | 29.6 us: 1.05x slower                                                  |
| python_startup             | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                  |
| float                      | 74.2 ms                                                                | 78.2 ms: 1.05x slower                                                  |
| mdp                        | 2.47 sec                                                               | 2.62 sec: 1.06x slower                                                 |
| docutils                   | 2.59 sec                                                               | 2.78 sec: 1.07x slower                                                 |
| bench_mp_pool              | 89.4 ms                                                                | 96.7 ms: 1.08x slower                                                  |
| generators                 | 29.4 ms                                                                | 32.1 ms: 1.09x slower                                                  |
| dulwich_log                | 66.2 ms                                                                | 72.9 ms: 1.10x slower                                                  |
| sphinx                     | 992 ms                                                                 | 1.10 sec: 1.11x slower                                                 |
| pylint                     | 283 ms                                                                 | 315 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 4.35 sec                                                               | 4.85 sec: 1.12x slower                                                 |
| k_core                     | 2.07 sec                                                               | 2.31 sec: 1.12x slower                                                 |
| pickle_pure_python         | 320 us                                                                 | 357 us: 1.12x slower                                                   |
| many_optionals             | 1.03 ms                                                                | 1.17 ms: 1.13x slower                                                  |
| async_generators           | 341 ms                                                                 | 388 ms: 1.14x slower                                                   |
| subparsers                 | 22.6 ms                                                                | 25.8 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 731 ms                                                                 | 837 ms: 1.14x slower                                                   |
| thrift                     | 758 us                                                                 | 871 us: 1.15x slower                                                   |
| xml_etree_generate         | 84.9 ms                                                                | 97.5 ms: 1.15x slower                                                  |
| json_dumps                 | 11.2 ms                                                                | 12.9 ms: 1.15x slower                                                  |
| logging_silent             | 98.6 ns                                                                | 114 ns: 1.15x slower                                                   |
| sqlglot_v2_normalize       | 103 ms                                                                 | 120 ms: 1.16x slower                                                   |
| 2to3                       | 256 ms                                                                 | 298 ms: 1.16x slower                                                   |
| unpickle_pure_python       | 221 us                                                                 | 257 us: 1.16x slower                                                   |
| nqueens                    | 82.9 ms                                                                | 96.8 ms: 1.17x slower                                                  |
| deepcopy_reduce            | 2.77 us                                                                | 3.25 us: 1.17x slower                                                  |
| pprint_pformat             | 1.48 sec                                                               | 1.73 sec: 1.17x slower                                                 |
| sqlglot_v2_optimize        | 52.2 ms                                                                | 61.2 ms: 1.17x slower                                                  |
| deepcopy                   | 266 us                                                                 | 313 us: 1.17x slower                                                   |
| django_template            | 36.1 ms                                                                | 42.7 ms: 1.18x slower                                                  |
| genshi_xml                 | 50.9 ms                                                                | 60.4 ms: 1.19x slower                                                  |
| tomli_loads                | 1.96 sec                                                               | 2.34 sec: 1.19x slower                                                 |
| sympy_expand               | 465 ms                                                                 | 555 ms: 1.19x slower                                                   |
| xml_etree_process          | 59.4 ms                                                                | 70.9 ms: 1.19x slower                                                  |
| sympy_sum                  | 156 ms                                                                 | 186 ms: 1.20x slower                                                   |
| logging_simple             | 6.09 us                                                                | 7.33 us: 1.20x slower                                                  |
| spectral_norm              | 93.0 ms                                                                | 112 ms: 1.20x slower                                                   |
| sqlalchemy_imperative      | 19.6 ms                                                                | 23.7 ms: 1.21x slower                                                  |
| chaos                      | 57.1 ms                                                                | 69.0 ms: 1.21x slower                                                  |
| sympy_integrate            | 19.5 ms                                                                | 23.6 ms: 1.21x slower                                                  |
| comprehensions             | 17.0 us                                                                | 20.6 us: 1.21x slower                                                  |
| pyflate                    | 422 ms                                                                 | 514 ms: 1.22x slower                                                   |
| sympy_str                  | 275 ms                                                                 | 335 ms: 1.22x slower                                                   |
| sqlalchemy_declarative     | 129 ms                                                                 | 158 ms: 1.22x slower                                                   |
| sqlglot_v2_transpile       | 1.58 ms                                                                | 1.93 ms: 1.22x slower                                                  |
| scimark_fft                | 323 ms                                                                 | 397 ms: 1.23x slower                                                   |
| telco                      | 7.41 ms                                                                | 9.10 ms: 1.23x slower                                                  |
| scimark_sor                | 113 ms                                                                 | 139 ms: 1.23x slower                                                   |
| regex_compile              | 127 ms                                                                 | 156 ms: 1.23x slower                                                   |
| raytrace                   | 263 ms                                                                 | 325 ms: 1.23x slower                                                   |
| shortest_path              | 443 ms                                                                 | 548 ms: 1.24x slower                                                   |
| crypto_pyaes               | 71.3 ms                                                                | 88.2 ms: 1.24x slower                                                  |
| logging_format             | 6.73 us                                                                | 8.36 us: 1.24x slower                                                  |
| fannkuch                   | 401 ms                                                                 | 498 ms: 1.24x slower                                                   |
| deltablue                  | 3.11 ms                                                                | 3.88 ms: 1.25x slower                                                  |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.59 ms: 1.25x slower                                                  |
| meteor_contest             | 102 ms                                                                 | 128 ms: 1.25x slower                                                   |
| hexiom                     | 6.08 ms                                                                | 7.63 ms: 1.25x slower                                                  |
| genshi_text                | 22.6 ms                                                                | 28.4 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 198 us: 1.26x slower                                                   |
| go                         | 113 ms                                                                 | 144 ms: 1.28x slower                                                   |
| connected_components       | 398 ms                                                                 | 509 ms: 1.28x slower                                                   |
| scimark_monte_carlo        | 65.6 ms                                                                | 83.9 ms: 1.28x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 144 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 4.47 ms                                                                | 5.72 ms: 1.28x slower                                                  |
| mako                       | 12.2 ms                                                                | 15.7 ms: 1.29x slower                                                  |
| python_startup_no_site     | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                                  |
| richards                   | 42.6 ms                                                                | 55.1 ms: 1.29x slower                                                  |
| deepcopy_memo              | 30.4 us                                                                | 39.3 us: 1.29x slower                                                  |
| richards_super             | 48.4 ms                                                                | 64.1 ms: 1.33x slower                                                  |
| nbody                      | 101 ms                                                                 | 139 ms: 1.38x slower                                                   |
| coverage                   | 78.7 ms                                                                | 109 ms: 1.39x slower                                                   |
| bench_thread_pool          | 1.06 ms                                                                | 3.16 ms: 2.99x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250326-3.14.0a6+-7bb41ae-NOGIL/bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae.json: html5lib

- Geometric mean (including insignificant results): 1.111x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x