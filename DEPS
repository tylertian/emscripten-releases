# Copyright 2019 the V8 project authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

vars = {
  'binaryen_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/binaryen',
  'emscripten_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten',
  'fastcomp_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp',
  'fastcomp_clang_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp-clang',
  'llvm_project_url': 'https://github.com/llvm/llvm-project',
  'wabt_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/wabt',
  'waterfall_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/waterfall',
  # TODO: clang, v8 for testing, Gcc for torture tests, llvm test-suite

  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling binaryen
  # and whatever else without interference from each other.
  'binaryen_revision': 'f0ec4b02fb797387040c65d63f690b3856b1183e',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling emscripten
  # and whatever else without interference from each other.
  'emscripten_revision': '7545a66c871997e1c42ed0079bda0d09eb70e774',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp
  # and whatever else without interference from each other.
  'fastcomp_revision': 'af16ece2f07be6b83674cc3729249f8aca720fc2',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp_clang
  # and whatever else without interference from each other.
  'fastcomp_clang_revision': '0479dcd35c96e2c5d1485dc8719e9c840a95b057',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling llvm_project
  # and whatever else without interference from each other.
  'llvm_project_revision': '9134f84ba4eaf593653739047b0c4fffa94c9ad0',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling wabt
  # and whatever else without interference from each other.
  'wabt_revision': '8ab47309e20748c465e28773c92cef7029f5e410',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling waterfall
  # and whatever else without interference from each other.
  'waterfall_revision': '8a69fd9644646c7a63cbdcdbd175cd44036f7b12',
}

deps = {
  # TODO: refactor waterfall script such that we don't have to use the hardcoded work dir.
  'waterfall/src/work/binaryen': Var('binaryen_url') + '@' + Var('binaryen_revision'),
  'waterfall/src/work/emscripten': Var('emscripten_url') + '@' + Var('emscripten_revision'),
  'waterfall/src/work/emscripten-fastcomp': Var('fastcomp_url') + '@' + Var('fastcomp_revision'),
  'waterfall/src/work/emscripten-fastcomp/tools/clang': Var('fastcomp_clang_url') + '@' + Var('fastcomp_clang_revision'),
  'waterfall/src/work/llvm-project': Var('llvm_project_url') + '@' + Var('llvm_project_revision'),
  'waterfall/src/work/wabt': Var('wabt_url') + '@' + Var('wabt_revision'),
  'waterfall': Var('waterfall_url') + '@' + Var('waterfall_revision'),
}