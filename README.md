# SwiftUI-Grid
SwiftUI grid arrangement, adaptive arrangement according to screen size.
# The first part
![IMG_1068](https://github.com/S-way520/SwiftUI-Grid/assets/95877651/feb4f432-86d3-4e51-bbd3-26f36d1b4e62)
![IMG_1067](https://github.com/S-way520/SwiftUI-Grid/assets/95877651/20c47020-9d68-41e6-ba57-5cd47dbad5ed)
# The second part
Code file 1
```swift
import SwiftUI
@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}
```
Code file 2
```swift
import SwiftUI
struct ContentView: View {
    @State private var gridColumns: [GridItem] = [GridItem(.adaptive(minimum: 380), spacing: 10)]
    var body: some View {
        ScrollView {
            LazyVGrid(columns: gridColumns) {
                HStack {Spacer()}
                .frame(width: .infinity, height: 400)
                .background(Color.red)
                
                HStack {Spacer()}
                .frame(width: .infinity, height: 400)
                .background(Color.green)
                
                HStack {Spacer()}
                    .frame(width: .infinity, height: 400)
                    .background(Color.gray)
                
                HStack {Spacer()}
                    .frame(width: .infinity, height: 400)
                    .background(Color.orange)
                
                HStack {Spacer()}
                    .frame(width: .infinity, height: 400)
                    .background(Color.gray)
                
                HStack {Spacer()}
                    .frame(width: .infinity, height: 400)
                    .background(Color.cyan)
            }
            
        }
    }
}
``'
