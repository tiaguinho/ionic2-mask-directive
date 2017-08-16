# ionic2-mask-directive

Ionic2MaskDirective help you add mask on ion-input with just a directive and a very simple configuration.

## Install

```bash
npm i ionic2-mask-directive --save
```

## Import directive

Import the directive into your app module.

```typescript
import {Ionic2MaskDirective} from "ionic2-mask-directive";

@NgModule({
    declarations: [
        MyApp,
        Ionic2MaskDirective,
        HomePage
    ],
    imports: [
        BrowserModule,
        IonicModule.forRoot(MyApp),
        HttpModule
    ],
    bootstrap: [IonicApp],
    entryComponents: [
        MyApp,
        HomePage
    ],
    providers: [
        StatusBar,
        SplashScreen,
        {provide: ErrorHandler, useClass: IonicErrorHandler}        
    ]
})
export class AppModule {
}
```

## Usage

To configure the mask, you can use 3 types of characters.

* \# - any type of char;
* 9 - only numbers;
* A - only letters;

## Example

```html
<!-- phone number in Brasil -->
<ion-input type="text" mask="(99) 9999-9999" placeholder="Phone" [(ngModel)]="user.phone" required></ion-input>
<!-- brasilian document -->
<ion-input type="text" mask="999.999.999-99" placeholder="CPF" [(ngModel)]="user.document" required></ion-input>
```

## Contribute

Any pull-request and issue is more than welcome.

## License

[The MIT License (MIT) Copyright (c) 2013](http://opensource.org/licenses/MIT) 
 