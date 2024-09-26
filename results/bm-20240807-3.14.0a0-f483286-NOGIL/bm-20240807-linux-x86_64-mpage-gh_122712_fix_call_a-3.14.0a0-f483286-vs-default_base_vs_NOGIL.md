# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 443 ms                                                                | 646 ms: 1.46x slower                                                 |
| docutils       | 3.99 sec                                                              | 5.06 sec: 1.27x slower                                               |
| html5lib       | 93.9 ms                                                               | 140 ms: 1.49x slower                                                 |
| tornado_http   | 220 ms                                                                | 367 ms: 1.67x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 1.31 sec                                                              | 1.15 sec: 1.14x faster                                               |
| async_tree_io           | 1.30 sec                                                              | 1.25 sec: 1.04x faster                                               |
| async_tree_none         | 547 ms                                                                | 585 ms: 1.07x slower                                                 |
| async_tree_memoization  | 676 ms                                                                | 751 ms: 1.11x slower                                                 |
| async_tree_cpu_io_mixed | 832 ms                                                                | 933 ms: 1.12x slower                                                 |
| asyncio_tcp             | 990 ms                                                                | 1.12 sec: 1.13x slower                                               |
| asyncio_tcp_ssl         | 2.81 sec                                                              | 3.36 sec: 1.19x slower                                               |
| async_generators        | 590 ms                                                                | 753 ms: 1.28x slower                                                 |
| coroutines              | 31.6 ms                                                               | 42.1 ms: 1.33x slower                                                |
| Geometric mean          | (ref)                                                                 | 1.08x slower                                                         |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 117 ms                                                                | 196 ms: 1.68x slower                                                 |
| nbody          | 113 ms                                                                | 284 ms: 2.50x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.60x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 35.4 ms                                                               | 39.2 ms: 1.11x slower                                                |
| regex_compile  | 182 ms                                                                | 295 ms: 1.62x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                         |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.6 us                                                               | 14.1 us: 1.11x faster                                                |
| pickle_dict          | 46.0 us                                                               | 43.9 us: 1.05x faster                                                |
| unpickle_list        | 7.17 us                                                               | 7.94 us: 1.11x slower                                                |
| unpickle             | 19.8 us                                                               | 22.0 us: 1.11x slower                                                |
| xml_etree_iterparse  | 152 ms                                                                | 179 ms: 1.17x slower                                                 |
| json_dumps           | 14.7 ms                                                               | 17.7 ms: 1.20x slower                                                |
| json_loads           | 37.6 us                                                               | 45.4 us: 1.21x slower                                                |
| xml_etree_generate   | 111 ms                                                                | 164 ms: 1.48x slower                                                 |
| tomli_loads          | 2.65 sec                                                              | 4.20 sec: 1.58x slower                                               |
| xml_etree_process    | 80.5 ms                                                               | 135 ms: 1.68x slower                                                 |
| pickle_pure_python   | 403 us                                                                | 778 us: 1.93x slower                                                 |
| unpickle_pure_python | 281 us                                                                | 567 us: 2.02x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.27x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.1 ms                                                               | 29.3 ms: 1.33x slower                                                |
| python_startup_no_site | 15.2 ms                                                               | 20.7 ms: 1.37x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.35x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 47.1 ms                                                               | 77.1 ms: 1.64x slower                                                |
| genshi_text     | 30.4 ms                                                               | 54.2 ms: 1.78x slower                                                |
| genshi_xml      | 64.1 ms                                                               | 118 ms: 1.84x slower                                                 |
| mako            | 16.7 ms                                                               | 32.1 ms: 1.92x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.79x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| bench_mp_pool            | 22.0 ms                                                               | 16.8 ms: 1.31x faster                                                |
| gc_traversal             | 5.71 ms                                                               | 4.63 ms: 1.23x faster                                                |
| create_gc_cycles         | 2.26 ms                                                               | 1.92 ms: 1.18x faster                                                |
| async_tree_io_tg         | 1.31 sec                                                              | 1.15 sec: 1.14x faster                                               |
| pickle                   | 15.6 us                                                               | 14.1 us: 1.11x faster                                                |
| pickle_dict              | 46.0 us                                                               | 43.9 us: 1.05x faster                                                |
| async_tree_io            | 1.30 sec                                                              | 1.25 sec: 1.04x faster                                               |
| async_tree_none          | 547 ms                                                                | 585 ms: 1.07x slower                                                 |
| regex_v8                 | 35.4 ms                                                               | 39.2 ms: 1.11x slower                                                |
| unpickle_list            | 7.17 us                                                               | 7.94 us: 1.11x slower                                                |
| unpickle                 | 19.8 us                                                               | 22.0 us: 1.11x slower                                                |
| async_tree_memoization   | 676 ms                                                                | 751 ms: 1.11x slower                                                 |
| async_tree_cpu_io_mixed  | 832 ms                                                                | 933 ms: 1.12x slower                                                 |
| asyncio_tcp              | 990 ms                                                                | 1.12 sec: 1.13x slower                                               |
| sqlite_synth             | 3.86 us                                                               | 4.44 us: 1.15x slower                                                |
| xml_etree_iterparse      | 152 ms                                                                | 179 ms: 1.17x slower                                                 |
| json                     | 6.94 ms                                                               | 8.22 ms: 1.19x slower                                                |
| asyncio_tcp_ssl          | 2.81 sec                                                              | 3.36 sec: 1.19x slower                                               |
| json_dumps               | 14.7 ms                                                               | 17.7 ms: 1.20x slower                                                |
| pylint                   | 491 ms                                                                | 590 ms: 1.20x slower                                                 |
| meteor_contest           | 161 ms                                                                | 194 ms: 1.20x slower                                                 |
| pathlib                  | 29.5 ms                                                               | 35.6 ms: 1.21x slower                                                |
| json_loads               | 37.6 us                                                               | 45.4 us: 1.21x slower                                                |
| bench_thread_pool        | 3.48 ms                                                               | 4.33 ms: 1.24x slower                                                |
| docutils                 | 3.99 sec                                                              | 5.06 sec: 1.27x slower                                               |
| async_generators         | 590 ms                                                                | 753 ms: 1.28x slower                                                 |
| telco                    | 10.8 ms                                                               | 13.8 ms: 1.28x slower                                                |
| coverage                 | 110 ms                                                                | 146 ms: 1.32x slower                                                 |
| python_startup           | 22.1 ms                                                               | 29.3 ms: 1.33x slower                                                |
| coroutines               | 31.6 ms                                                               | 42.1 ms: 1.33x slower                                                |
| python_startup_no_site   | 15.2 ms                                                               | 20.7 ms: 1.37x slower                                                |
| scimark_fft              | 457 ms                                                                | 635 ms: 1.39x slower                                                 |
| pycparser                | 1.65 sec                                                              | 2.29 sec: 1.39x slower                                               |
| generators               | 41.0 ms                                                               | 57.5 ms: 1.40x slower                                                |
| mdp                      | 3.65 sec                                                              | 5.16 sec: 1.41x slower                                               |
| 2to3                     | 443 ms                                                                | 646 ms: 1.46x slower                                                 |
| scimark_sparse_mat_mult  | 6.27 ms                                                               | 9.23 ms: 1.47x slower                                                |
| deepcopy                 | 378 us                                                                | 556 us: 1.47x slower                                                 |
| fannkuch                 | 527 ms                                                                | 776 ms: 1.47x slower                                                 |
| xml_etree_generate       | 111 ms                                                                | 164 ms: 1.48x slower                                                 |
| html5lib                 | 93.9 ms                                                               | 140 ms: 1.49x slower                                                 |
| nqueens                  | 107 ms                                                                | 161 ms: 1.50x slower                                                 |
| crypto_pyaes             | 101 ms                                                                | 152 ms: 1.50x slower                                                 |
| sympy_integrate          | 29.3 ms                                                               | 44.3 ms: 1.51x slower                                                |
| pyflate                  | 710 ms                                                                | 1.09 sec: 1.53x slower                                               |
| typing_runtime_protocols | 225 us                                                                | 356 us: 1.58x slower                                                 |
| tomli_loads              | 2.65 sec                                                              | 4.20 sec: 1.58x slower                                               |
| thrift                   | 1.10 ms                                                               | 1.77 ms: 1.61x slower                                                |
| spectral_norm            | 157 ms                                                                | 253 ms: 1.61x slower                                                 |
| bpe_tokeniser            | 6.32 sec                                                              | 10.3 sec: 1.62x slower                                               |
| regex_compile            | 182 ms                                                                | 295 ms: 1.62x slower                                                 |
| deepcopy_reduce          | 3.59 us                                                               | 5.84 us: 1.63x slower                                                |
| django_template          | 47.1 ms                                                               | 77.1 ms: 1.64x slower                                                |
| sqlglot_normalize        | 148 ms                                                                | 242 ms: 1.64x slower                                                 |
| tornado_http             | 220 ms                                                                | 367 ms: 1.67x slower                                                 |
| float                    | 117 ms                                                                | 196 ms: 1.68x slower                                                 |
| xml_etree_process        | 80.5 ms                                                               | 135 ms: 1.68x slower                                                 |
| pprint_safe_repr         | 953 ms                                                                | 1.64 sec: 1.72x slower                                               |
| comprehensions           | 22.1 us                                                               | 38.3 us: 1.74x slower                                                |
| richards_super           | 71.3 ms                                                               | 124 ms: 1.74x slower                                                 |
| logging_simple           | 8.58 us                                                               | 15.0 us: 1.75x slower                                                |
| scimark_monte_carlo      | 91.3 ms                                                               | 160 ms: 1.76x slower                                                 |
| pprint_pformat           | 1.94 sec                                                              | 3.45 sec: 1.78x slower                                               |
| genshi_text              | 30.4 ms                                                               | 54.2 ms: 1.78x slower                                                |
| sympy_str                | 376 ms                                                                | 673 ms: 1.79x slower                                                 |
| deepcopy_memo            | 38.8 us                                                               | 69.7 us: 1.80x slower                                                |
| richards                 | 61.1 ms                                                               | 110 ms: 1.80x slower                                                 |
| genshi_xml               | 64.1 ms                                                               | 118 ms: 1.84x slower                                                 |
| logging_format           | 9.79 us                                                               | 18.5 us: 1.89x slower                                                |
| logging_silent           | 134 ns                                                                | 254 ns: 1.90x slower                                                 |
| mako                     | 16.7 ms                                                               | 32.1 ms: 1.92x slower                                                |
| pickle_pure_python       | 403 us                                                                | 778 us: 1.93x slower                                                 |
| sqlglot_optimize         | 72.6 ms                                                               | 143 ms: 1.98x slower                                                 |
| chaos                    | 85.3 ms                                                               | 169 ms: 1.98x slower                                                 |
| hexiom                   | 8.52 ms                                                               | 17.2 ms: 2.01x slower                                                |
| unpickle_pure_python     | 281 us                                                                | 567 us: 2.02x slower                                                 |
| sqlglot_transpile        | 2.25 ms                                                               | 4.62 ms: 2.05x slower                                                |
| scimark_lu               | 148 ms                                                                | 303 ms: 2.05x slower                                                 |
| scimark_sor              | 166 ms                                                                | 342 ms: 2.05x slower                                                 |
| sympy_expand             | 600 ms                                                                | 1.26 sec: 2.10x slower                                               |
| sympy_sum                | 213 ms                                                                | 465 ms: 2.19x slower                                                 |
| raytrace                 | 343 ms                                                                | 765 ms: 2.23x slower                                                 |
| go                       | 180 ms                                                                | 446 ms: 2.48x slower                                                 |
| deltablue                | 4.55 ms                                                               | 11.3 ms: 2.49x slower                                                |
| nbody                    | 113 ms                                                                | 284 ms: 2.50x slower                                                 |
| sqlglot_parse            | 1.75 ms                                                               | 4.43 ms: 2.54x slower                                                |
| unpack_sequence          | 56.2 ns                                                               | 211 ns: 3.74x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.45x slower                                                         |

Benchmark hidden because not significant (9): async_tree_cpu_io_mixed_tg, pidigits, asyncio_websockets, regex_effbot, regex_dna, xml_etree_parse, async_tree_none_tg, pickle_list, async_tree_memoization_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.14x