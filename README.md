# Cambiar-Tint-Color-de-una-imagen-en-Swift

```swift
// (Swift4)
if let logo = UIImage(named: "logo"){
	self.ImageLogo.image = logo.withTintColor(UIColor(red: CGFloat(255)/255.0, green: CGFloat(89)/255.0, blue: CGFloat(0), alpha: CGFloat(1)))
}
```

```swift
// (Swift 3)
extension UIImage {
    func tint(with color: UIColor) -> UIImage {
        var image = withRenderingMode(.alwaysTemplate)
        UIGraphicsBeginImageContextWithOptions(size, false, scale)
        color.set()

        image.draw(in: CGRect(origin: .zero, size: size))
        image = UIGraphicsGetImageFromCurrentImageContext()!
        UIGraphicsEndImageContext()
        return image
    }
}
```
