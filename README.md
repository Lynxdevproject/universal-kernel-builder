# 🔧 Universal Kernel Builder CI

A lightweight GitHub Actions workflow for compiling Android kernels via form-based input. Designed for both beginner and advanced maintainers, this builder enables seamless kernel packaging with AnyKernel3—no CLI required, no server dependency.

## 🛠️ Features

- ✅ UI-based trigger with customizable inputs (kernel source, branch, defconfig, packaging toggle)
- ✅ Compiler-safe build flags (`LLVM=1 LLVM_IAS=1`) for improved compatibility
- ✅ Uses official toolchains: Clang (Android 14) + GCC 4.9 (arm64 + arm32)
- ✅ Auto-packaging with AnyKernel3 (optional)
- ✅ Output ZIP includes developer name and timestamp
- ✅ Artifact upload support for compiled kernel and packaging assets

## 📦 Output ZIP Format

## 🚀 How to Use

1. Go to your repository's **Actions tab**
2. Select **Universal Kernel Builder**
3. Click **Run workflow**
4. Fill out the form inputs:
   - 🔗 Kernel source repo (e.g., `https://github.com/...`)
   - 🌿 Branch name (e.g., `main`)
   - 🧪 Defconfig (e.g., `begonia_user_defconfig`)
   - 📦 Toggle AnyKernel3 packaging (checkbox)
   - 👤 Developer name (branding)
   - 📝 Custom ZIP name (optional)

5. Wait for CI magic—your build artifact will be uploaded when complete!

## 🧙 Toolchain Structure

```plaintext
📂 aarch64-linux-android-4.9 → 64-bit GCC
📂 arm-linux-androideabi-4.9 → 32-bit GCC
📂 clang/ → Android 14 Clang archive (r487747c)

## 🧪 Example Devices

- Redmi Note 8 Pro (begonia)
- POCO X3 Pro (vayu)
- Realme Narzo Series
- Realme 6 Series
- Redmi Note 7 (lavender)
- Redmi K20 Pro (raphael)
- Mi A2 (jasmine_sprout)
- Xiaomi Mi 10T Pro (apollo)
- POCO F5 (marble)

## 🙌 Credits

- **Toolchain sources**  
  Prebuilt GCC & Clang archives sourced from [LineageOS](https://github.com/LineageOS) and [AOSP](https://android.googlesource.com/platform/prebuilts/clang)

- **Kernel packaging**  
  [AnyKernel3](https://github.com/osm0sis/AnyKernel3) maintained by osm0sis

- **Workflow inspiration**  
  Remake inspired by [Zclkk](https://github.com/zclkk)'s config.env builder and the minimalist CI flow of [OrangeFox Recovery](https://github.com/OrangeFoxRecovery)

- **Workflow integration**  
  Final builder designed and refined for universal kernel compilation with GitHub UI trigger and artifact export


## 🙌 Credits

- **Toolchain sources**  
  Prebuilt GCC & Clang archives sourced from [LineageOS](https://github.com/LineageOS) and [AOSP](https://android.googlesource.com/platform/prebuilts/clang)

- **Kernel packaging**  
  [AnyKernel3](https://github.com/osm0sis/AnyKernel3) maintained by osm0sis

- **Workflow inspiration**  
  Remake inspired by [Zclkk](https://github.com/zclkk)'s config.env builder and the minimalist CI flow of [OrangeFox Recovery](https://github.com/OrangeFoxRecovery)

- **Workflow integration**  
  Final builder designed and refined for universal kernel compilation with GitHub UI trigger and artifact export
