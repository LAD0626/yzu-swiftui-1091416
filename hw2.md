<h1>HW1</h1>
    
```swift

import SwiftUI
import EmojiPicker
import UIKit

let five = "\u{1F590}"
let victory = "\u{270C}"
let rais = "\u{270a}"
var choice=[five,victory,rais]

struct ContentView:View{
    @State var p1_c = 0
    @State var p2_c = 0
    @State var win = 2
    var body: some View {
        ZStack{
            Image("Bkp")
                .resizable()
                .scaledToFill()
                .edgesIgnoringSafeArea(.all)
            VStack(alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/) {
                Text("剪刀石頭布")
                    .font(.system(size:45))
                Spacer()
                Text(String(choice[p1_c])+"   "+String(choice[p2_c]))
                    .font(.system(size:100))
                    .frame(alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                Text(String("p1"+"          "+"p2"))
                    .font(.system(size:50))
                    .frame(alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                Spacer()
                Button(action:{
                    withAnimation{
                        p1_c=Int.random(in:0...2) 
                        p2_c=Int.random(in:0...2)
                        if p1_c-p2_c == 1 || p2_c-p1_c == 2{
                            win=0
                        }
                        if p2_c-p1_c == 1 || p1_c-p2_c == 2{
                            win=1
                        }
                        if p1_c == p2_c{
                            win=2
                        }
                    }
                },label:{
                    Text("start")
                        .frame(width: 300, height: 80 )
                        .font(.system(size: 50))
                        .background(Color.purple)
                        .foregroundColor(.white)
                        .border(Color.purple, width: 5)
                        .cornerRadius(20)
                })
                if win == 0{
                    Text("P1 is winnr")
                        .font(.system(size: 30))
                }
                if win == 1{
                    Text("P2 is winnr")
                        .font(.system(size: 30))
                }
                if win == 2{
                    Text("Tie")
                        .font(.system(size: 30))
                }
            }
            .frame(maxWidth: .infinity, maxHeight:500)
        }
    }
}
```
<img width="40%"  src="https://github.com/LAD0626/yzu-swiftui-1091416/blob/main/hw2-1091416.png">
