# Rules for test files
# Applied when Claude is working with *.test.* or *.spec.* files

- Always use describe/it pattern, never test() directly
- Mock all external dependencies
- Use meaningful test descriptions that read as sentences
- Keep each test focused on a single behavior
- Use beforeEach for shared setup, afterEach for cleanup
- Never use real API keys or external services in tests
