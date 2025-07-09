## Semantic Kernel Blog Post Generator

This repository demonstrates how to build a complete blog post generator using Microsoft Semantic Kernel with OpenAI and Azure OpenAI services. It showcases how to interact with chat, image, and audio models to produce a rich, multi-modal content pipeline.

### Repository Objective

- **Showcase Semantic Kernel Capabilities**: Illustrate how to use Microsoft Semantic Kernel to invoke text completion, image generation, and audio synthesis.  
- **End-to-End Workflow**: Provide a full example that takes a user-supplied topic and generates:  
  - A structured WordPress-compatible blog post  
  - A featured image for the post  
  - An audio narration of the post content  
- **Hands-On Learning**: Serve as a practical exercise for students to explore kernel configuration, prompt engineering, and multi-service integration.

### What You Will Build

By working through this project, you will create:

1. **A .NET Console Application** that:  
   - Prompts the user for a blog post topic  
   - Uses the Semantic Kernel `InvokePromptAsync` API to generate Gutenberg block–formatted content  
   - Calls the Kernel `ITextToImageService` to produce a featured image URL  
   - Cleans the generated HTML and uses `ITextToAudioService` to synthesize an MP3 narration  
2. **Environment Configuration**:  
   - Reading OpenAI and Azure API keys and endpoints from environment variables  
   - Switching between OpenAI and Azure providers seamlessly in code  
3. **Utility Functions**:  
   - A helper to strip Gutenberg comments and HTML tags for clean audio input  
   - Console output with Spectre.Console for a rich CLI experience

### Learning Outcomes

By building this repository from scratch, you will learn:

- **Kernel Initialization**: How to configure multiple AI service providers (OpenAI and Azure OpenAI) in Semantic Kernel.  
- **Prompt Engineering**: Structuring prompts to generate rich, formatted outputs (e.g., Gutenberg blocks for WordPress).  
- **Multi-Modal AI Integration**:  
  - Text completion for content creation  
  - Text-to-image generation with DALL·E  
  - Text-to-audio synthesis with OpenAI or Azure voices  
- **C# Implementation Patterns**:  
  - Asynchronous programming with `async`/`await`  
  - Dependency injection and service resolution (`GetRequiredService<>()`)  
  - Regular expressions for content cleaning  
- **CLI UX Enhancements**: Using Spectre.Console to display status spinners and colored output for better user feedback.

---

### Prerequisites

- .NET 7.0 SDK or later  
- Environment variables set:  
  - `SKCourseOpenAIKey`  
  - `SKCourseAzureRegion`  
  - `SKCourseAzureKey`

### Getting Started

1. **Clone the Repo**  
   ```bash
   git clone https://github.com/your-org/semantic-kernel-blog-generator.git
   cd semantic-kernel-blog-generator
   ```

2. **Set Environment Variables** (Windows PowerShell example)  
   ```powershell
   $env:SKCourseOpenAIKey = "YOUR_OPENAI_KEY"
   $env:SKCourseAzureRegion = "YOUR_AZURE_REGION"
   $env:SKCourseAzureKey    = "YOUR_AZURE_KEY"
   ```

3. **Run the Application**  
   ```bash
   dotnet run --project src/BlogPostGenerator
   ```

4. **Follow the Prompts**: Enter a topic and watch the blog content, image URL, and audio file path appear in the console.

---

Feel free to customize prompts, models, and output formats as you experiment with the Semantic Kernel!
