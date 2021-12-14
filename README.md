# antd-img-crop-v2

An image cropper for Ant Design [Upload](https://ant.design/components/upload/).

## Install

```sh
yarn add antd-img-crop

# npm install antd-img-crop
```

## Usage

```jsx harmony
import ImgCrop from 'antd-img-crop';
import {Upload} from 'antd';

const Demo = () => (
    <ImgCrop>
        <Upload>+ Add image</Upload>
    </ImgCrop>
);
```

## Props

| Prop          | Type                 | Default        | Description                                                           |
| ------------- | -------------------- | -------------- | --------------------------------------------------------------------- |
| aspect        | `number`             | `1 / 1`        | Aspect of crop area , `width / height`                                |
| shape         | `string`             | `'rect'`       | Shape of crop area, `'rect'` or `'round'`                             |
| grid          | `boolean`            | `false`        | Show grid of crop area (third-lines)                                  |
| quality       | `number`             | `0.4`          | Image quality, `0 ~ 1`                                                |
| fillColor     | `string`             | `'white'`      | Fill color when cropped image smaller than canvas                     |
| zoom          | `boolean`            | `true`         | Enable zoom for image                                                 |
| rotate        | `boolean`            | `false`        | Enable rotate for image                                               |
| minZoom       | `number`             | `1`            | Minimum zoom factor                                                   |
| maxZoom       | `number`             | `3`            | Maximum zoom factor                                                   |
| modalTitle    | `string`             | `'Edit image'` | Title of modal                                                        |
| modalWidth    | `number` \| `string` | `520`          | Width of modal in pixels number or percentages                        |
| modalOk       | `string`             | `'OK'`         | Text of modal confirm button                                          |
| modalCancel   | `string`             | `'Cancel'`     | Text of modal cancel button                                           |
| onModalOk     | `function`           | -              | Call when click modal confirm button                                  |
| onModalCancel | `function`           | -              | Call when click modal mask, top right "x", or cancel button           |
| beforeCrop    | `function`           | -              | Call before modal open, if return `false`, it'll not open             |
| onUploadFail  | `function`           | -              | Call when upload failed                                               |
| cropperProps  | `object`             | -              | Props of [react-easy-crop] (\* [existing props] cannot be overridden) |

## Styles

To prevent overwriting the custom styles to `antd`, `antd-img-crop` does not import the style files of components.

Therefore, if your project configured `babel-plugin-import` and no `Modal` or `Slider` were used, you need to import the
styles manually:

```js
import 'antd/es/modal/style';
import 'antd/es/slider/style';
```
