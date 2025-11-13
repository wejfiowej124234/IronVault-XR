# Contributing to IronVault-XR

Thank you for your interest in contributing to IronVault-XR! 🥽

## 🚧 Current Status

This project is in the **early planning phase**. We're currently:
- Designing the FFI architecture
- Evaluating AR platform capabilities
- Defining the API surface
- Building the community

## 🤝 How to Contribute

### For Early Contributors

#### 1. 💡 Architecture & Design
- Review and comment on the FFI interface design
- Suggest improvements to the AR user experience
- Propose security enhancements
- Share AR development best practices

#### 2. 📝 Documentation
- Help document AR platform quirks and limitations
- Write integration guides for different devices
- Create tutorial content
- Improve existing documentation

#### 3. 🔬 Research & Prototyping
- Test FFI integration with Rust backend
- Prototype AR payment flows on real devices
- Benchmark performance on target hardware
- Research Starlink integration strategies

#### 4. 🧪 Testing & Validation
- Test on different AR devices
- Validate UX assumptions with real users
- Performance testing on target hardware
- Security vulnerability assessment

## 📋 Contribution Process

### For Discussion & Ideas

1. Check existing [GitHub Issues](https://github.com/DarkCrab-Rust/IronVault-XR/issues)
2. Open a new issue with appropriate label:
   - `enhancement` - Feature proposals
   - `architecture` - Design discussions
   - `platform` - Platform-specific topics
   - `documentation` - Docs improvements
3. Participate constructively in discussions

### For Code (Once Development Begins)

1. Fork the repository
2. Create a feature branch
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes
4. Follow code style guidelines
5. Write tests
6. Commit with clear messages
7. Push and create a Pull Request

## 📐 Code Style Guidelines (Future)

### Rust Core
- Follow [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/)
- Use `rustfmt` for formatting
- Use `clippy` for linting
- Document all public FFI functions
- Add safety comments for `unsafe` blocks

### FFI Interface
```rust
// Good: Clear documentation for foreign callers
/// Signs a transaction with the wallet's private key.
/// 
/// # Safety
/// - `tx_data` must be a valid null-terminated UTF-8 string
/// - Caller must free the returned string with `ironvault_free_string`
#[no_mangle]
pub unsafe extern "C" fn ironvault_sign_transaction(
    tx_data: *const c_char
) -> *mut c_char {
    // Implementation
}
```

### Platform Code
- **Swift**: Follow [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)
- **C#**: Follow [.NET Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
- **Kotlin**: Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)

## 🔍 Review Process

- All PRs require at least one approving review
- Platform-specific changes need review from platform expert
- FFI changes need extra scrutiny for safety
- Security-related changes require security team review

## 💬 Communication

- **GitHub Issues**: For bugs, features, and tasks
- **GitHub Discussions**: For questions and ideas
- **Discord** (coming soon): Real-time collaboration

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for helping build the future of AR cryptocurrency payments!** 🦀🥽

Last Updated: November 9, 2025

