# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 418 ms                                                                 | 410 ms: 1.02x faster                                                  |
| docutils       | 3.39 sec                                                               | 3.31 sec: 1.02x faster                                                |
| html5lib       | 107 ms                                                                 | 105 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines       | 31.2 ms                                                                | 28.9 ms: 1.08x faster                                                 |
| async_generators | 489 ms                                                                 | 480 ms: 1.02x faster                                                  |
| asyncio_tcp      | 584 ms                                                                 | 581 ms: 1.01x faster                                                  |
| Geometric mean   | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 182 ms: 1.02x faster                                                  |
| nbody          | 202 ms                                                                 | 199 ms: 1.01x faster                                                  |
| float          | 150 ms                                                                 | 149 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 231 ms                                                                 | 212 ms: 1.09x faster                                                  |
| regex_v8       | 24.8 ms                                                                | 25.1 ms: 1.01x slower                                                 |
| regex_effbot   | 3.12 ms                                                                | 3.20 ms: 1.03x slower                                                 |
| regex_dna      | 181 ms                                                                 | 186 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 424 us                                                                 | 389 us: 1.09x faster                                                  |
| pickle_pure_python   | 627 us                                                                 | 577 us: 1.09x faster                                                  |
| pickle_dict          | 33.8 us                                                                | 31.6 us: 1.07x faster                                                 |
| xml_etree_process    | 95.4 ms                                                                | 89.3 ms: 1.07x faster                                                 |
| xml_etree_generate   | 116 ms                                                                 | 109 ms: 1.07x faster                                                  |
| tomli_loads          | 3.25 sec                                                               | 3.12 sec: 1.04x faster                                                |
| xml_etree_iterparse  | 110 ms                                                                 | 106 ms: 1.04x faster                                                  |
| json_dumps           | 15.2 ms                                                                | 14.7 ms: 1.03x faster                                                 |
| json_loads           | 29.9 us                                                                | 29.4 us: 1.02x faster                                                 |
| unpickle             | 14.8 us                                                                | 14.6 us: 1.02x faster                                                 |
| xml_etree_parse      | 135 ms                                                                 | 134 ms: 1.01x faster                                                  |
| pickle_list          | 5.14 us                                                                | 5.13 us: 1.00x faster                                                 |
| unpickle_list        | 4.99 us                                                                | 5.01 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                 |
| python_startup         | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 40.9 ms                                                                | 36.2 ms: 1.13x faster                                                 |
| genshi_xml      | 83.3 ms                                                                | 74.3 ms: 1.12x faster                                                 |
| django_template | 65.1 ms                                                                | 59.2 ms: 1.10x faster                                                 |
| mako            | 20.9 ms                                                                | 20.2 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                          |

All benchmarks:
===============

| Benchmark                | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_lu               | 252 ms                                                                 | 216 ms: 1.17x faster                                                  |
| deepcopy_memo            | 54.3 us                                                                | 46.7 us: 1.16x faster                                                 |
| pprint_safe_repr         | 1.35 sec                                                               | 1.17 sec: 1.15x faster                                                |
| pprint_pformat           | 2.79 sec                                                               | 2.42 sec: 1.15x faster                                                |
| typing_runtime_protocols | 260 us                                                                 | 226 us: 1.15x faster                                                  |
| deepcopy                 | 439 us                                                                 | 387 us: 1.13x faster                                                  |
| genshi_text              | 40.9 ms                                                                | 36.2 ms: 1.13x faster                                                 |
| genshi_xml               | 83.3 ms                                                                | 74.3 ms: 1.12x faster                                                 |
| unpack_sequence          | 154 ns                                                                 | 137 ns: 1.12x faster                                                  |
| sqlglot_normalize        | 184 ms                                                                 | 164 ms: 1.12x faster                                                  |
| sqlglot_optimize         | 91.6 ms                                                                | 82.1 ms: 1.12x faster                                                 |
| deepcopy_reduce          | 4.57 us                                                                | 4.10 us: 1.11x faster                                                 |
| django_template          | 65.1 ms                                                                | 59.2 ms: 1.10x faster                                                 |
| regex_compile            | 231 ms                                                                 | 212 ms: 1.09x faster                                                  |
| unpickle_pure_python     | 424 us                                                                 | 389 us: 1.09x faster                                                  |
| pickle_pure_python       | 627 us                                                                 | 577 us: 1.09x faster                                                  |
| coroutines               | 31.2 ms                                                                | 28.9 ms: 1.08x faster                                                 |
| pickle_dict              | 33.8 us                                                                | 31.6 us: 1.07x faster                                                 |
| bpe_tokeniser            | 6.20 sec                                                               | 5.79 sec: 1.07x faster                                                |
| xml_etree_process        | 95.4 ms                                                                | 89.3 ms: 1.07x faster                                                 |
| xml_etree_generate       | 116 ms                                                                 | 109 ms: 1.07x faster                                                  |
| hexiom                   | 12.6 ms                                                                | 11.8 ms: 1.06x faster                                                 |
| richards_super           | 109 ms                                                                 | 104 ms: 1.05x faster                                                  |
| logging_simple           | 12.4 us                                                                | 11.8 us: 1.04x faster                                                 |
| pathlib                  | 22.3 ms                                                                | 21.4 ms: 1.04x faster                                                 |
| spectral_norm            | 163 ms                                                                 | 156 ms: 1.04x faster                                                  |
| tomli_loads              | 3.25 sec                                                               | 3.12 sec: 1.04x faster                                                |
| logging_format           | 13.6 us                                                                | 13.1 us: 1.04x faster                                                 |
| chaos                    | 124 ms                                                                 | 119 ms: 1.04x faster                                                  |
| xml_etree_iterparse      | 110 ms                                                                 | 106 ms: 1.04x faster                                                  |
| logging_silent           | 215 ns                                                                 | 208 ns: 1.04x faster                                                  |
| mako                     | 20.9 ms                                                                | 20.2 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult  | 6.18 ms                                                                | 5.97 ms: 1.03x faster                                                 |
| pycparser                | 1.73 sec                                                               | 1.68 sec: 1.03x faster                                                |
| richards                 | 89.7 ms                                                                | 86.7 ms: 1.03x faster                                                 |
| pylint                   | 423 ms                                                                 | 409 ms: 1.03x faster                                                  |
| sympy_str                | 545 ms                                                                 | 527 ms: 1.03x faster                                                  |
| json_dumps               | 15.2 ms                                                                | 14.7 ms: 1.03x faster                                                 |
| pyflate                  | 782 ms                                                                 | 758 ms: 1.03x faster                                                  |
| sympy_sum                | 384 ms                                                                 | 372 ms: 1.03x faster                                                  |
| sympy_integrate          | 33.2 ms                                                                | 32.2 ms: 1.03x faster                                                 |
| nqueens                  | 116 ms                                                                 | 112 ms: 1.03x faster                                                  |
| json                     | 5.51 ms                                                                | 5.35 ms: 1.03x faster                                                 |
| sqlglot_transpile        | 3.33 ms                                                                | 3.24 ms: 1.03x faster                                                 |
| sympy_expand             | 1.06 sec                                                               | 1.03 sec: 1.03x faster                                                |
| comprehensions           | 30.6 us                                                                | 29.8 us: 1.03x faster                                                 |
| go                       | 299 ms                                                                 | 292 ms: 1.02x faster                                                  |
| docutils                 | 3.39 sec                                                               | 3.31 sec: 1.02x faster                                                |
| deltablue                | 9.11 ms                                                                | 8.90 ms: 1.02x faster                                                 |
| dulwich_log              | 105 ms                                                                 | 103 ms: 1.02x faster                                                  |
| 2to3                     | 418 ms                                                                 | 410 ms: 1.02x faster                                                  |
| scimark_monte_carlo      | 127 ms                                                                 | 124 ms: 1.02x faster                                                  |
| pidigits                 | 186 ms                                                                 | 182 ms: 1.02x faster                                                  |
| scimark_fft              | 418 ms                                                                 | 410 ms: 1.02x faster                                                  |
| async_generators         | 489 ms                                                                 | 480 ms: 1.02x faster                                                  |
| meteor_contest           | 138 ms                                                                 | 136 ms: 1.02x faster                                                  |
| coverage                 | 103 ms                                                                 | 101 ms: 1.02x faster                                                  |
| sqlite_synth             | 2.47 us                                                                | 2.43 us: 1.02x faster                                                 |
| json_loads               | 29.9 us                                                                | 29.4 us: 1.02x faster                                                 |
| thrift                   | 1.29 ms                                                                | 1.27 ms: 1.02x faster                                                 |
| unpickle                 | 14.8 us                                                                | 14.6 us: 1.02x faster                                                 |
| sqlglot_parse            | 2.87 ms                                                                | 2.82 ms: 1.02x faster                                                 |
| telco                    | 9.32 ms                                                                | 9.19 ms: 1.01x faster                                                 |
| bench_thread_pool        | 3.51 ms                                                                | 3.46 ms: 1.01x faster                                                 |
| nbody                    | 202 ms                                                                 | 199 ms: 1.01x faster                                                  |
| crypto_pyaes             | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| create_gc_cycles         | 1.13 ms                                                                | 1.11 ms: 1.01x faster                                                 |
| html5lib                 | 107 ms                                                                 | 105 ms: 1.01x faster                                                  |
| scimark_sor              | 273 ms                                                                 | 271 ms: 1.01x faster                                                  |
| xml_etree_parse          | 135 ms                                                                 | 134 ms: 1.01x faster                                                  |
| bench_mp_pool            | 72.7 ms                                                                | 72.1 ms: 1.01x faster                                                 |
| float                    | 150 ms                                                                 | 149 ms: 1.01x faster                                                  |
| asyncio_tcp              | 584 ms                                                                 | 581 ms: 1.01x faster                                                  |
| gc_traversal             | 2.47 ms                                                                | 2.46 ms: 1.01x faster                                                 |
| fannkuch                 | 565 ms                                                                 | 562 ms: 1.00x faster                                                  |
| python_startup_no_site   | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                 |
| python_startup           | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| pickle_list              | 5.14 us                                                                | 5.13 us: 1.00x faster                                                 |
| unpickle_list            | 4.99 us                                                                | 5.01 us: 1.01x slower                                                 |
| mdp                      | 3.17 sec                                                               | 3.19 sec: 1.01x slower                                                |
| raytrace                 | 631 ms                                                                 | 637 ms: 1.01x slower                                                  |
| regex_v8                 | 24.8 ms                                                                | 25.1 ms: 1.01x slower                                                 |
| generators               | 40.7 ms                                                                | 41.3 ms: 1.01x slower                                                 |
| regex_effbot             | 3.12 ms                                                                | 3.20 ms: 1.03x slower                                                 |
| regex_dna                | 181 ms                                                                 | 186 ms: 1.03x slower                                                  |
| Geometric mean           | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): pickle, asyncio_tcp_ssl, asyncio_websockets

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x