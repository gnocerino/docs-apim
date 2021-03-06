# Enable or Disable Home Page

When the developer portal required to present corporate branding it’s a common requirement to have a landing page. The default landing page is the API listing page. But when we enable home page, there will be an additional landing page. It can be customized based on the design requirements. 

### The home page has four sections.
1. carousel
2. First Description and the listing of APIs filtered by a given tag ( provided via the theme file ).
3. Second description and the listing of APIs filtered by a given tag ( provided via the theme file ).
4. Contact us section

 ![enable or disable home page](../../../../assets/img/learn/enable-or-disable-home-page.png) 

## Landing page configuration options

Following JSON defines the look and feel and behavior of the landing page.


``` js
landingPage: {
    active: true,
    carousel: {
        active: true,
        slides: [
            {
                src: '/site/public/images/landing/01.jpg',
                title: 'Lorem <span>ipsum</span> dolor sit amet',
                content:
                    'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer felis lacus, placerat vel condimentum in, porta a urna. Suspendisse dolor diam, vestibulum at molestie dapibus, semper eget ex. Morbi sit amet euismod tortor.',
            },
            {
                src: '/site/public/images/landing/02.jpg',
                title: 'Curabitur <span>malesuada</span> arcu sapien',
                content:
                    'Curabitur malesuada arcu sapien, suscipit egestas purus efficitur vitae. Etiam vulputate hendrerit venenatis. ',
            },
            {
                src: '/site/public/images/landing/03.jpg',
                title: 'Nam vel ex <span>feugiat</span> nunc laoreet',
                content:
                    'Nam vel ex feugiat nunc laoreet elementum. Duis sed nibh condimentum, posuere risus a, mollis diam. Vivamus ultricies, augue id pulvinar semper, mauris lorem bibendum urna, eget tincidunt quam ex ut diam.',
            },
        ],
    },
    listByTag: {
        active: true,
        content: [
            {
                tag: 'finance',
                title: 'Checkout our Finance APIs',
                description:
                    'We offers online payment solutions and has more than 123 million customers worldwide. The WSO2 Finane API makes powerful functionality available to developers by exposing various features of our platform. Functionality includes but is not limited to invoice management, transaction processing and account management.',
                maxCount: 5,
            },
            {
                tag: 'weather',
                title: 'Checkout our Weather APIs',
                description:
                    'We offers online payment solutions and has more than 123 million customers worldwide. The WSO2 Finane API makes powerful functionality available to developers by exposing various features of our platform. Functionality includes but is not limited to invoice management, transaction processing and account management.',
                maxCount: 5,
            },
        ],
    },
    parallax: {
        active: true,
        content: [
            {
                src: '/site/public/images/landing/parallax1.jpg',
                title: 'Lorem <span>ipsum</span> dolor sit amet',
                content:
                    'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer felis lacus, placerat vel condimentum in, porta a urna. Suspendisse dolor diam, vestibulum at molestie dapibus, semper eget ex. Morbi sit amet euismod tortor.',
            },
            {
                src: '/site/public/images/landing/parallax2.jpg',
                title: 'Nam vel ex <span>feugiat</span> nunc laoreet',
                content:
                    'Nam vel ex feugiat nunc laoreet elementum. Duis sed nibh condimentum, posuere risus a, mollis diam. Vivamus ultricies, augue id pulvinar semper, mauris lorem bibendum urna, eget tincidunt quam ex ut diam.',
            },
        ],
    },
}
```

| Option | type | Values | Description |
| ------ | -- | ----------- | ----------- |
| active | boolean | true, false | If true the feature is enabled. If false(default), the feature is disabled  |
| carousel.active | boolean | true, false | If true( default ) the carousel section is visible. If false carousel section is hidden. |
| carousel.slides | array | |  Provide the content for the carousel animation at the page top. Slide is a json of following format. {src: 'path-to-slide-image/image.png', title: 'Title text with <span>special text</span>',content:'Slide description' }  |
| listByTag.active | boolean | true, false | If true( default ) the listByTag section is visible. If false listByTag section is hidden. |
listByTag.content | array | | Provide the content for the API grouping. It's an array of JSON where the JSON of following format. { tag: 'tag-name', title: 'Title for tag-name', description: '', maxCount: 5 } .|
| parallax.active | boolean | true, false | If true( default ) the parallax scrolling section is visible. If false parallax scrolling section is hidden. | 

The landing page provides a headstart for developers who tries to rebrand the devportal for their needs. If the requirements are much complicated, then you need to override the relevant components. The step to override only specific react components can be found [here](advanced-customization.md).

