# 3D Agency Loading Screen 🎨


[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Three.js](https://img.shields.io/badge/Three.js-black?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
[![React Three Fiber](https://img.shields.io/badge/React%20Three%20Fiber-black?style=for-the-badge&logo=three.js&logoColor=white)](https://docs.pmnd.rs/react-three-fiber)

## 📝 Description

A professional 3D loading screen implementation using React Three Fiber and Suspense. This project demonstrates how to handle loading states for 3D models and textures in a web application, providing a smooth user experience during resource loading.

## 🎥 Preview


## 🎓 Credits

This project is based on the teachings from [Wawa Sensei's](https://wawasensei.dev/) comprehensive React Three Fiber course. Special thanks to Wawa Sensei for providing excellent tutorials and guidance in 3D web development.

## 🚀 Features

- Full-screen loading interface
- Progress bar with real-time loading percentage
- Smooth transitions using CSS animations
- Proper resource preloading
- Suspense integration for 3D models
- Responsive design

## 🛠️ Technical Implementation

### Loading Screen Components
- Custom LoadingScreen component with progress tracking
- useProgress hook from @react-three/drei
- CSS animations for smooth transitions
- BEM methodology for structured styling

### 3D Resource Management
- Suspense for asynchronous loading
- Model preloading capabilities
- Optimized resource loading
- Progress tracking for multiple resources

## 💻 Usage

### Basic Setup
```jsx
import { Suspense } from "react";
import { Canvas } from "@react-three/fiber";
import { LoadingScreen } from "./components/LoadingScreen";
import { Experience } from "./components/Experience";

function App() {
  return (
    <>
      <LoadingScreen />
      <Canvas>
        <Suspense fallback={null}>
          <Experience />
        </Suspense>
      </Canvas>
    </>
  );
}
```

### Progress Tracking
```jsx
import { useProgress } from "@react-three/drei";

const LoadingScreen = () => {
  const { progress, active } = useProgress();
  return (
    <div className={`loading-screen ${active ? "" : "loading-screen--hidden"}`}>
      {/* Loading screen content */}
    </div>
  );
};
```

## 🎯 Best Practices

1. **Optimization First**: Consider optimizing models and textures before implementing a loading screen
2. **Strategic Loading**: Use preloading for critical resources
3. **User Experience**: Provide visual feedback during loading
4. **Resource Management**: Implement proper resource cleanup
5. **Performance**: Consider lazy loading for non-critical assets

## 📚 Additional Resources

- [Wawa Sensei's Course](https://wawasensei.dev/)
- [React Three Fiber Documentation](https://docs.pmnd.rs/react-three-fiber)
- [Three.js Documentation](https://threejs.org/docs/)

## 🤝 Contributing

Feel free to contribute to this project by submitting issues or pull requests.
