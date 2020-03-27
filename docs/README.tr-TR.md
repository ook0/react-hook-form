<div align="center">
    <p align="center">
        <a href="https://react-hook-form.com" title="React Hook Form - Simple React forms validation">
            <img src="https://raw.githubusercontent.com/bluebill1049/react-hook-form/master/website/logo.png" alt="React Hook Form Logo - React hook custom hook for form validation" width="300px" />
        </a>
    </p>
</div>

<p align="center">Kullanımı kolay doğrulama özelliğine sahip, efektik, esnek ve genişletilebilir formlar.</p>

<div align="center">

[![npm downloads](https://img.shields.io/npm/dm/react-hook-form.svg?style=flat-square)](https://www.npmjs.com/package/react-hook-form)
[![npm](https://img.shields.io/npm/dt/react-hook-form.svg?style=flat-square)](https://www.npmjs.com/package/react-hook-form)
![dep](https://badgen.net/david/dep/bluebill1049/react-hook-form)
[![npm](https://badgen.net/bundlephobia/minzip/react-hook-form)](https://badgen.net/bundlephobia/minzip/react-hook-form)
[![Coverage Status](https://coveralls.io/repos/github/bluebill1049/react-hook-form/badge.svg?branch=master)](https://coveralls.io/github/bluebill1049/react-hook-form?branch=master)

[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=React+hooks+for+form+validation+without+the+hassle&url=https://github.com/bluebill1049/react-hook-form)&nbsp;[![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/react-hook-form)

</div>

<div align="center">
    <p align="center">
        <a href="https://react-hook-form.com" title="React Hook Form - Simple React forms validation">
            <img src="https://raw.githubusercontent.com/bluebill1049/react-hook-form/master/website/example.gif" alt="React Hook Form video - React custom hook for form validation" width="100%" />
        </a>
    </p>
</div>

<a href="https://github.com/react-hook-form/react-hook-form">🇦🇺English</a> | <a href="./docs/README.zh-CN.md">🇨🇳 简体中文</a> | <a href="./docs/README.ja-JP.md">🇯🇵 日本語</a> | <a href="./docs/README.ko-KR.md">🇰🇷한국어</a> | <a href="./docs/README.fr-FR.md">🇫🇷Français</a> | <a href="./docs/README.it-IT.md">🇮🇹Italiano</a> | <a href="./docs/README.pt-BR.md">🇧🇷Português</a> | <a href="./docs/README.es-ES.md">🇪🇸Español</a> | <a href="./docs/README.ru-RU.md">🇷🇺Русский</a> | 🇪🇸Türkçe

## Features

- Performans ve DX düşünülerek tasarlandı.
- Embrace uncontrolled form validation
- Kontrollü formun performasını arttır
- Bağımlılık içermeyen [Küçük boyut](https://bundlephobia.com/result?p=react-hook-form@latest)
- Doğrulama için HTML standardını uygular
- React Native ile uyumlu
- [Yup](https://github.com/jquense/yup), [Joi](https://github.com/hapijs/joi), [Superstruct](https://github.com/ianstormtaylor/superstruct) veya özel destekler.
- Native tarayıcı doğrulamasını destekler
- Build forms quickly with the [form builder](https://react-hook-form.com/form-builder)

## Yükle

    $ npm install react-hook-form

## Linkler

- [Motivasyon](https://medium.com/@bruce1049/form-validation-with-hook-in-3kb-c5414edf7d64)
- [Video öğretici](https://www.youtube.com/watch?v=-mFXqOaqgZk&t)
- [Başlamk için](https://react-hook-form.com/get-started)
- [API](https://react-hook-form.com/api)
- [Örnekler](https://github.com/bluebill1049/react-hook-form/tree/master/examples)
- [Demo](https://react-hook-form.com)
- [Form Oluşturucu](https://react-hook-form.com/form-builder)
- [SSS](https://react-hook-form.com/faqs)

## Hızlı Başlangıç

```jsx
import React from 'react';
import { useForm } from 'react-hook-form';

function App() {
  const { register, handleSubmit, errors } = useForm(); // initialise the hook
  const onSubmit = data => {
    console.log(data);
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input name="firstname" ref={register} /> {/* register an input */}

      <input name="lastname" ref={register({ required: true })} />
      {errors.lastname && 'Soyisim gerekli.'}

      <input name="age" ref={register({ pattern: /\d+/ })} />
      {errors.age && 'Yaş için lütfen sayı girin.'}

      <input type="submit" />
    </form>
  );
}
```

## Backers

Thanks goes to all our backers! [[Become a backer](https://opencollective.com/react-hook-form#backer)].

<a href="https://opencollective.com/react-hook-form#backers">
    <img src="https://opencollective.com/react-hook-form/backers.svg?width=950" />
</a>

## Organizations

Thanks goes to these wonderful organizations. [[Contribute](https://opencollective.com/react-hook-form/contribute)]

<a href="https://github.com/react-hook-form/react-hook-form/graphs/contributors">
    <img src="https://opencollective.com/react-hook-form/organizations.svg?width=950" />
</a>

## Contributors

Thanks goes to these wonderful people. [[Become a contributor](CONTRIBUTING.md)].

<a href="https://github.com/react-hook-form/react-hook-form/graphs/contributors">
    <img src="https://opencollective.com/react-hook-form/contributors.svg?width=950" />
</a>
