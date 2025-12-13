# covered_calls_web

[![Deploy to GitHub Pages](https://github.com/tonytmtsh/covered_calls_web/actions/workflows/deploy.yml/badge.svg)](https://github.com/tonytmtsh/covered_calls_web/actions/workflows/deploy.yml)

This repository hosts the Flutter web application **"covered_calls"**, which is automatically built and deployed to GitHub Pages.

## 🌐 Live Demo

The application is deployed at: **https://tonytmtsh.github.io/covered_calls_web/**

## 📦 About

This repository contains a Flutter web application for covered calls that is automatically deployed to GitHub Pages using GitHub Actions. Every push to the `main` branch triggers an automated build and deployment process.

## 🚀 Deployment Workflow

The deployment is fully automated through GitHub Actions (`.github/workflows/deploy.yml`). Here's how it works:

### Workflow Steps

1. **Checkout Code** - Retrieves the latest code from the repository
2. **Setup Flutter** - Installs Flutter SDK (stable channel)
3. **Enable Web Support** - Configures Flutter for web development
4. **Get Dependencies** - Runs `flutter pub get` to fetch all dependencies
5. **Build for Web** - Compiles the Flutter app to web with the correct base href (`/covered_calls_web/`)
6. **Upload Artifact** - Prepares the built files (`build/web` directory) for GitHub Pages
7. **Deploy to GitHub Pages** - Publishes the application to GitHub Pages

### Workflow Features

- ✅ **Automatic deployment** on every push to `main` branch
- ✅ **Proper permissions** configured for GitHub Pages deployment
- ✅ **Concurrency control** to prevent multiple simultaneous deployments
- ✅ **Uses official GitHub Actions** for reliable deployment

## ⚙️ Enabling GitHub Pages

To enable GitHub Pages for this repository, follow these steps:

1. Navigate to your repository on GitHub
2. Click on **Settings** (in the repository menu)
3. Scroll down to the **Pages** section in the left sidebar
4. Under **Source**, select **GitHub Actions** from the dropdown menu
5. Save the changes

Once enabled, the workflow will automatically deploy to GitHub Pages whenever you push to the `main` branch.

## 📱 Pushing Your Flutter App

To add your Flutter application to this repository:

1. **Create your Flutter app** (if not already created):
   ```bash
   flutter create covered_calls
   ```

2. **Navigate to your Flutter app directory**:
   ```bash
   cd covered_calls
   ```

3. **Initialize git and add this repository as remote**:
   ```bash
   git init
   git remote add origin https://github.com/tonytmtsh/covered_calls_web.git
   ```

4. **Add and commit your Flutter app files**:
   ```bash
   git add .
   git commit -m "Add covered_calls Flutter app"
   ```

5. **Push to the main branch**:
   ```bash
   git pull origin main --rebase
   git push origin main
   ```

6. **Monitor the deployment**:
   - Go to the **Actions** tab in your GitHub repository
   - Watch the workflow run and ensure it completes successfully
   - Once complete, visit https://tonytmtsh.github.io/covered_calls_web/

## 🛠️ Technical Details

- **App Name**: `covered_calls`
- **Repository**: `covered_calls_web`
- **Deployment URL**: https://tonytmtsh.github.io/covered_calls_web/
- **Build Output**: `build/web`
- **Base Href**: `/covered_calls_web/`
- **Flutter Channel**: `stable`

## 📄 License

This project is open source and available under the MIT License.
