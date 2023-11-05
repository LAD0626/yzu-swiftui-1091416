<h1>HW1</h1>
    
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack {
            Image("Bkp")
                .resizable()
                .scaledToFill()
                .edgesIgnoringSafeArea(.all) // 忽略安全区域，使图像占据整个屏幕
            VStack {
                VStack{
                    Text("    ")
                        .font(.system(size: 30))
                    Image("Me") // 2. 上半部分中间放一张图片
                        .resizable()
                        .scaledToFit()
                        .frame(width: 700, height: 450)
                    Text("spend your life in your ")
                        .font(.largeTitle)
                        .rotationEffect(.degrees(-30), anchor: .topLeading)
                        .offset(x: -220, y: -390)
                        .foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/) .font(.system(size: 50))
                    Text("own way")
                        .font(.largeTitle)
                        .rotationEffect(.degrees(-30), anchor: .topLeading)
                        .offset(x: -210, y: -420)
                        .foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/)
                     .font(.system(size: 50))
                    
                                    }.frame(maxHeight: UIScreen.main.bounds.height*0.5)
            
                VStack {
                    HStack {
                        Text("林安滴\(Image(systemName: "person.crop.circle.fill.badge.plus"))").frame(maxWidth: .infinity, maxHeight: UIScreen.main.bounds.height).foregroundColor(.black)
                        .font(.system(size: 100))
                        
                    }
                    HStack {
                        Text("").frame(maxWidth: .infinity, maxHeight:  UIScreen.main.bounds.height)
                        Text("1091416").frame(maxWidth: .infinity, maxHeight:  UIScreen.main.bounds.height).foregroundColor(.black).font(.system(size: 70))
                        
                    }
                    HStack {
                        Text("Andie").frame(maxWidth: .infinity, maxHeight:  UIScreen.main.bounds.height).foregroundColor(.black).font(.system(size: 90))
                        Text("").frame(maxWidth: .infinity, maxHeight:  UIScreen.main.bounds.height)
                        
                    }
                }
                .frame(maxWidth: .infinity, maxHeight: UIScreen.main.bounds.height*0.4)
            }
            .background(Color.white.opacity(0)) // 设置底部区域的背景颜色和透明度
                // 下半部分分六块区域，分别显示文字
        
        }
    }
}
```
<img width="40%"  src="https://github.com/LAD0626/yzu-swiftui-1091416/blob/main/hw1-1091416.png">
