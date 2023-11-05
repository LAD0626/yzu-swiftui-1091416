<h1>HW1</h1>
    
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Text("我的收藏櫃")
                .font(.largeTitle)
                .padding(.top, 20)
            
            // 创建3x3的方格
            ForEach(0..<3) { row in
                HStack {
                    ForEach(0..<3) { column in
                        ZStack {
                            RoundedRectangle(cornerRadius: 10)
                                .fill(Color.blue)
                                .frame(width: 200, height: 200)
                            
                            VStack {
                                Image("Cat")
                                    .resizable()
                                    .frame(width: 180, height: 170)
                                
                                Text("\(row * 3 + column + 1)")
                                    .font(.caption)
                            }
                        }
                    }
                }
            }
        }
    }
}
```
<img width="40%"  src="https://github.com/LAD0626/yzu-swiftui-1091416/blob/main/hw3-1091416.png">
