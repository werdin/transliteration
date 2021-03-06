# Transliteration

Small PHP library for transliteration.

* Scrutinizer [![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/fre5h/transliteration/badges/quality-score.png?s=e04dee642516971b6922584ae403b923d9dd8aa3)](https://scrutinizer-ci.com/g/fre5h/transliteration/)
[![Build Status](https://scrutinizer-ci.com/g/fre5h/transliteration/badges/build.png?b=master)](https://scrutinizer-ci.com/g/fre5h/transliteration/build-status/master)
[![Code Coverage](https://scrutinizer-ci.com/g/fre5h/transliteration/badges/coverage.png?s=741891f1f3d6f39dc01eb6d1b2199f0816f05b34)](https://scrutinizer-ci.com/g/fre5h/transliteration/)
* Travis CI [![Build Status](https://secure.travis-ci.org/fre5h/transliteration.png?branch=master)](https://travis-ci.org/fre5h/transliteration)
* Packagist.org [![License](https://poser.pugx.org/fresh/transliteration/license.png)](https://packagist.org/packages/fresh/transliteration)
[![Latest Stable Version](https://poser.pugx.org/fresh/transliteration/v/stable.png)](https://packagist.org/packages/fresh/transliteration)
[![Total Downloads](https://poser.pugx.org/fresh/transliteration/downloads.png)](https://packagist.org/packages/fresh/transliteration)
* VersionEye [![Dependency Status](https://www.versioneye.com/user/projects/52ea18a3ec13755c2f000055/badge.svg)](https://www.versioneye.com/user/projects/52ea18a3ec13755c2f000055)
[![Reference Status](https://www.versioneye.com/php/fresh:transliteration/reference_badge.svg)](https://www.versioneye.com/php/fresh:transliteration/references)
* HHVM [![HHVM Status](http://hhvm.h4cc.de/badge/fresh/transliteration.svg)](http://hhvm.h4cc.de/package/fresh/transliteration)
* CodeCov [![codecov.io](https://codecov.io/github/fre5h/transliteration/coverage.svg?branch=master)](https://codecov.io/github/fre5h/transliteration?branch=master)

[![SensioLabsInsight](https://insight.sensiolabs.com/projects/ad4d26d5-cd6b-4fa6-8287-7d74234a2106/big.png)](https://insight.sensiolabs.com/projects/ad4d26d5-cd6b-4fa6-8287-7d74234a2106)

## Requirements

* PHP 5.4 *and later*

## Install via Composer

```php composer.phar require fresh/transliteration='v1.1.0'```

## Available transliteration methods

<table>
    <thead>
        <tr>
            <th>From</th>
            <th>To</th>
            <th>Rules</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <img src="/resources/images/ukraine-flag.png" alt="Ukrainian" title="Ukrainian" />
                <br />
                Ukrainian
            </td>
            <td>
                <img src="/resources/images/united-kingdom-flag.png" alt="English" title="English" />
                <br />
                English
            </td>
            <td>
                Resolution of the Cabinet of Ministers of Ukraine №55 dated January 27, 2010
                <br />
                http://zakon1.rada.gov.ua/laws/show/55-2010-%D0%BF
            </td>
        </tr>
    </tbody>
</table>

## Using

```php
<?php

namespace Acme;

use Fresh\Transliteration\Transliterator;
use Fresh\Transliteration\UkrainianToEnglish;

class Foo
{
    public function bar($text)
    {
        // You can use in this way
        $transliterator = new Transliterator();
        $transliteratedText = $transliterator->ukToEn($text);

        // Or like this
        $transliteratedText = UkrainianToEnglish::transliterate($ukrainianText);
    }
}
```

## Some examples of *Ukrainian-to-English* transliteration

<table>
    <thead>
        <tr>
            <th>
                <img src="/resources/images/ukraine-flag.png" alt="Ukrainian" title="Ukrainian" />
                <br />
                Ukrainian text
            </th>
            <th>
                <img src="/resources/images/united-kingdom-flag.png" alt="English" title="English" />
                <br />
                Transliterated text
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Володимир</td>
            <td>Volodymyr</td>
        </tr>
        <tr>
            <td>Богдан</td>
            <td>Bohdan</td>
        </tr>
        <tr>
            <td>Жанна</td>
            <td>Zhanna</td>
        </tr>
        <tr>
            <td>Наталія</td>
            <td>Nataliia</td>
        </tr>
        <tr>
            <td>Олексій</td>
            <td>Oleksii</td>
        </tr>
        <tr>
            <td>Уляна</td>
            <td>Uliana</td>
        </tr>
        <tr>
            <td>Юрій</td>
            <td>Yurii</td>
        </tr>
    </tbody>
</table>
