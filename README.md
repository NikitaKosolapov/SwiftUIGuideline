# SwiftUIGuideline

Гайдлайн по разработке приложений на SwiftUI

## Оглавление

* [Именование](#Именование)
* [Property wrappers](#Property-wrappers)
* [Организация кода](#Организация-кода)
* [Ограничения](#Ограничения)
* [Ссылки](#Ссылки)

## Именование

- Любая View должна иметь суффикс `View` или компонента. Например: HomeView, FilterButton, TitleLabel, ValueSlider
- Замыкания у View должны иметь префикс `on`. Например: onTap, onSelection, onChange, onDrag
- View-модель должна иметь префикс названия View и суффикс `Model`. Например: HomeViewModel, FilterViewModel

## Property wrappers

- @State - используется только внутри View
- @Binding - используется как внутри View, так и снаружи
- @StateObject - используется только внутри View. Жизненный цикл равен жизненному циклу View
- @ObservedObject - используется как внутри View, так и снаружи. Жизненный цикл управляется снаружи
- @EnvironmentObject - используется как внутри View, так и снаружи. Видимость объекта в рамках иерархии View
- @Environment - используется как внутри View, так и снаружи. Видимость во всем приложении
- @Published - используется как внутри ObservableObject, так и снаружи

## Организация кода

Соблюдайте следующую последовательность:
- public let
- public var
- internal let
- internal var
- private let
- private var
- public func
- public func
- internal func
- internal func
- private func
- private func

Последовательность врапперов:
- @Environment
- @EnvironmentObject
- @ObservedObject
- @StateObject
- @Binding
- @State

## Ограничения

- Не используйте вертикальные паддинги в вертикальном стэке и горизонтальные паддинги в горизонтальном стэке. Вместо этого для отступов используйте `Spacer()` с фиксированной высотой/шириной

## Ссылки

[Туториал от Apple](https://developer.apple.com/tutorials/swiftui/)  
[Первое знакомство с компонентами и переход из UIKit](https://github.com/SimpleBoilerplates/SwiftUI-Cheat-Sheet)  
[Все базовые вещи SwiftUI](https://fuckingswiftui.com)  
[Podlodka Crew #4](https://www.youtube.com/playlist?list=PLNSmyatBJig4yzwgVdhDJuSA4U8zhAqo7)  
[100 дней SwiftUI](https://www.hackingwithswift.com/100/swiftui)
