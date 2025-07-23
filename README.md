# Meta Quest MR Unity Template

[![Unity Version](https://img.shields.io/badge/Unity-6000.0.48f1-blue)](https://unity.com/releases/editor/whats-new/6000.0.48)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Android Build](https://github.com/afjk/Meta-Quest-MR-Unity-Template/actions/workflows/android-debug-build.yml/badge.svg)](https://github.com/afjk/Meta-Quest-MR-Unity-Template/actions/workflows/android-debug-build.yml)

A comprehensive Unity template designed for developing Mixed Reality (MR) applications on **Meta Quest 3** devices. This template provides a ready-to-use foundation with XR packages, optimized settings, and automated build workflows.

## 🚀 Features

- **Meta Quest 3 Ready**: Pre-configured for Meta Quest 3 MR development
- **Unity 6 Support**: Built with Unity 6000.0.48f1 for latest features and performance
- **XR Toolkit Integration**: Includes Unity XR Interaction Toolkit and Meta OpenXR packages
- **GitHub Actions CI/CD**: Automated Android builds on push to main branch
- **MR Optimized**: Pre-configured settings for Mixed Reality applications
- **Sample Scene**: Includes a basic sample scene to get started quickly

## 📋 Requirements

- **Unity 6000.0.48f1** or later
- **Android Build Support** module installed in Unity
- **Meta Quest 3** device for testing
- **Git LFS** (for large assets)

## 🛠️ Setup Instructions

For detailed setup instructions, please refer to the comprehensive guide on Qiita:

**📖 [Meta Quest MR Development Setup Guide](https://qiita.com/afjk/items/a57b07915feb0bed2d3a)**

### Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/afjk/Meta-Quest-MR-Unity-Template.git
   cd Meta-Quest-MR-Unity-Template
   ```

2. **Open in Unity**:
   - Launch Unity Hub
   - Click "Open" and select the cloned project folder
   - Unity will automatically import all packages and dependencies

3. **Configure XR Settings**:
   - The project is pre-configured for Meta Quest development
   - Verify XR settings in `Project Settings > XR Plug-in Management`

4. **Build and Deploy**:
   - Switch to Android platform (`File > Build Settings`)
   - Connect your Meta Quest 3 device
   - Build and Run to deploy to your device

## 🔄 GitHub Actions for Automated Builds

This template includes GitHub Actions workflow for automated Android builds. The CI/CD pipeline will automatically build your project when you push changes to the main branch.

### Setting Up Automated Builds

To use the automated build feature:

1. **Fork this repository** to your GitHub account

2. **Set up required Secrets** in your forked repository:
   - Go to `Settings > Secrets and variables > Actions`
   - Add the following repository secrets:
     - `UNITY_LICENSE`: Your Unity license file content (see below)
     - `UNITY_EMAIL`: Your Unity account email
     - `UNITY_PASSWORD`: Your Unity account password

### Unity License File (.ulf) Requirement

To run Unity on GitHub Actions, you need a Unity license file (.ulf), even for Personal licenses. The license file can be found at the following locations on your local machine:

#### License File Locations:
- **Windows**: `C:\ProgramData\Unity\Unity_lic.ulf`
- **Mac**: `/Library/Application Support/Unity/Unity_lic.ulf`
- **Linux**: `~/.local/share/unity3d/Unity/Unity_lic.ulf`

#### Setting Up the License:
1. Locate the `.ulf` file on your development machine
2. Copy the entire content of the file
3. Add it as the `UNITY_LICENSE` secret in your repository settings

For more detailed information about Unity license activation in CI/CD, refer to the [GameCI documentation](https://game.ci/docs/github/activation/).

## 📁 Project Structure

```
Meta-Quest-MR-Unity-Template/
├── Assets/
│   ├── Scenes/                 # Sample scenes
│   ├── XR/                     # XR configuration and settings
│   ├── XRI/                    # XR Interaction Toolkit components
│   ├── Settings/               # Project settings and configurations
│   └── ...
├── Packages/                   # Package dependencies
├── ProjectSettings/            # Unity project settings
├── .github/
│   └── workflows/
│       └── android-debug-build.yml  # GitHub Actions workflow
├── README.md
└── LICENSE
```

## 📦 Included Packages

This template includes the following key packages:

- **XR Packages**:
  - `com.unity.xr.openxr` (1.14.3) - OpenXR support
  - `com.unity.xr.meta-openxr` (2.2.0) - Meta OpenXR provider
  - `com.unity.xr.interaction.toolkit` (3.2.0) - XR interaction system
  - `com.unity.xr.hands` (1.6.0) - Hand tracking support
  - `com.unity.xr.management` (4.5.1) - XR management system

- **Rendering**:
  - `com.unity.render-pipelines.universal` (17.0.4) - URP for optimized rendering

- **Input**:
  - `com.unity.inputsystem` (1.14.0) - New Input System

## 🎯 Usage

1. **Start with the Sample Scene**: Open `Assets/Scenes/SampleScene.unity` to see a basic MR setup
2. **Customize for Your Needs**: Modify the scene and add your own MR content
3. **Test on Device**: Build and deploy to your Meta Quest 3 for testing
4. **Iterate**: Use the automated builds to test changes quickly

## 🔧 Development Tips

- **Performance**: This template is optimized for mobile VR/MR performance
- **Hand Tracking**: Hand tracking is pre-configured and ready to use
- **Mixed Reality**: The template supports both VR and MR modes
- **Testing**: Use Unity's XR Device Simulator for testing without a headset

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests to help improve this template.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Unity Technologies](https://unity.com/) for the Unity Engine and XR Toolkit
- [Meta](https://www.meta.com/) for Quest platform and OpenXR support
- [GameCI](https://game.ci/) for Unity CI/CD solutions
- The Unity XR development community for resources and support

## 📚 Additional Resources

- [Unity XR Documentation](https://docs.unity3d.com/Manual/XR.html)
- [Meta Quest Developer Documentation](https://developer.oculus.com/documentation/unity/)
- [XR Interaction Toolkit Documentation](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.0/manual/index.html)
- [GameCI Unity Documentation](https://game.ci/docs/github/getting-started)