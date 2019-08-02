# ModalWap 组件
> 手机端操作之前的相关事情

## 基本用法

[浏览器手机模式在线预览](https://output.jsbin.com/devewen)

<br>

<p>
  <button @click="status = true">{{ status ? '隐藏' : '显示' }}</button>
  <w-modal-wap v-if="status" @cancel="status = false" @ok="status = false">确定退出吗</w-modal-wap>
</p>
<br>
<br>

## API

### 属性

|参数|说明|类型|是否必填|默认值|
|---|----|---|-------|-----|
|okText|确定的文案|String|否|确定|
|canelText|取消的文案|String|否|取消|
|title|提示的文案 `1.0.0` 新增|String|否|提示|

### 方法

|参数|说明|返回值|
|---|----|---|
|ok|确定的回调|无|
|cancel|取消的回调|无|

<script>
import WModalWap from './ModalWap';

export default {
  data() {
    return {
      status: false,
    };
  },
  components: {
    WModalWap,
  },
};
</script>
