 [![BannerImage](banner.png)](https://www.zazz.io/)
# Xamarin to MAUI migration Dos and Don'ts with Code of Conduct Checklist
Migrating from **Xamarin.Forms** to **.NET MAUI (Multi-platform App UI)** marks a pivotal shift in cross-platform mobile development. As [Xamarin reaches its end of support](https://dotnet.microsoft.com/en-us/platform/support/policy/xamarin), MAUI emerges as its modern successor, offering a unified project structure, enhanced performance, and native access across Android, iOS, macOS, and Windows.

This guide is designed to support developers through the migration journey by highlighting:

* **Dos and Don’ts**: Practical advice to ensure a smooth transition, avoid common pitfalls, and embrace MAUI’s new paradigms.


* **Code of Conduct Checklist**: A structured, actionable checklist to help teams stay organized, maintain code quality, and ensure platform readiness throughout the migration process.

Whether you're planning a full-scale migration or just exploring MAUI’s capabilities, this guide will equip you with the insights and tools needed to modernize your app with confidence.

## **Dos and Don’ts**
Learn what to embrace and what to avoid. These practical tips will help you navigate the transition smoothly and make the most of MAUI’s capabilities.

Migrating is a significant step that brings many benefits, but it also requires careful planning. Here's a breakdown of Do's and Don'ts to help guide your migration process:

✅**Do's**

1. **Understand the Differences**

MAUI is the evolution of Xamarin.Forms, but with a new project structure, handler-based architecture, and better performance. Familiarize yourself with the single project structure, platform folders, and .NET 6/7+ features.

2. **Use the Upgrade Assistant**

Microsoft provides a .NET Upgrade Assistant to help automate parts of the migration. It helps convert project files and update NuGet packages.

3. **Refactor Gradually**

Start with non-UI logic (e.g., services, models) and migrate them to a .NET Standard or .NET 6+ class library. Then move to UI components, updating XAML and code-behind to match MAUI's structure.

4. **Test on All Platforms**

MAUI supports Android, iOS, macOS, and Windows. Test thoroughly on each target platform. Use Device Simulators and real devices for best coverage.

5. **Update Dependencies**

Ensure all third-party libraries are compatible with MAUI. Replace deprecated Xamarin libraries with their MAUI equivalents or alternatives.

6. **Leverage New Features**

Use Handlers instead of custom renderers. Explore Graphics APIs, Blazor Hybrid, and Essentials integration.

❌**Don'ts**

1. **Don't Migrate Everything at Once**

Avoid a big-bang migration. Instead, modularize and migrate incrementally.

2. **Don't Assume 1:1 Mapping**

Not all Xamarin.Forms APIs have direct equivalents in MAUI. Review the MAUI API changes and adapt accordingly.

3. **Don't Ignore Platform-Specific Code**

MAUI simplifies cross-platform development, but platform-specific code may still be needed. Use partial classes or platform folders for custom implementations.

4. **Don't Skip Performance Testing**

MAUI improves performance, but migration can introduce regressions. Profile and optimize your app post-migration.

5. **Don't Forget CI/CD Updates**

Update your build pipelines to use the new MAUI SDKs and tools. Ensure your DevOps environment supports .NET 6/7+ and MAUI workloads.

## Code of Conduct Checklist

Follow the detailed guide here. Use the Upgrade assistant extension on Windows or Upgrade assistant CLI available on Mac.

A structured, actionable checklist to help you:


* Stay organized
* Maintain code quality
* Ensure platform readiness
* Track progress across teams

**1. Preparation**

* Invest good amount of time on this step and prepare your Xamarin app for migration.
* Audit your Xamarin.Forms project for custom renderers, platform-specific code, and third-party libraries.
* Identify reusable components (models, services, business logic).
* Ensure your development environment is set up for MAUI.
* Visual Studio 2022 with MAUI workload 5) Backup your Xamarin.Forms project. (for reference)

**2. Project Setup**

* Create a new .NET MAUI project using Visual Studio.
* Familiarize yourself with the single project structure and platform folders.
* Add necessary NuGet packages compatible with MAUI.

**3. Code Migration**

* Shared Code Move models, services, and business logic to the new MAUI project or a shared .NET Standard/.NET 6+ library.
* UI Code Migrate XAML pages and update namespaces (xmlns).
* Replace deprecated controls/APIs with MAUI equivalents.
* Refactor custom renderers to Handlers if needed.
* Platform-Specific Code Move platform-specific implementations to appropriate folders (Platforms/Android, Platforms/iOS, etc.).
* Use partial classes or dependency injection for platform-specific logic.

**4. Configuration**


* Update App.xaml.cs and MainPage.xaml to match MAUI conventions.
* Configure fonts, images, and resources in Resources folder.
* Update MauiProgram.cs for dependency injection and service registration.
**5. Testing**

* Test UI and functionality on all target platforms (Android, iOS, Windows, macOS).
* Validate navigation, lifecycle events, and platform-specific features.
* Use logging and debugging tools to catch migration issues.

**6. Optimization**

* Profile performance and memory usage.
* Optimize startup time and UI responsiveness.
* Replace any inefficient code patterns.

**7. CI/CD & Deployment**

* Update build pipelines to use MAUI SDK.
* Configure platform-specific build settings.
* Test app packaging and deployment for each platform.

## Visual Studio Extensions
While [Maui migration guidelines](https://learn.microsoft.com/en-us/dotnet/maui/migration/) are very crisp and clear and there is no harm in using some extensions alongside which will also help in development.

Please go through their documentations to use it better and to its fullest.

* **[.NET MAUI Essentials](https://marketplace.visualstudio.com/items?itemName=MattLaceyLtd.MauiEssentials)**
* **[XAML Styler for Visual Studio 2022](https://marketplace.visualstudio.com/items?itemName=TeamXavalon.XAMLStyler2022)**
* **[Productivity Power Tools 2022](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.ProductivityPowerPack2022)**
* **[CodeDocumentor](https://marketplace.visualstudio.com/items?itemName=DanTurco.CodeDocumentor)**
---
Written by [Akshay Kulkarni](https://github.com/ak47akshaykulkarni), .NET MAUI Developer