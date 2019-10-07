# Swift 文档修订历史

本页面根据 [Document Revision History](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/RevisionHistory.html) 进行适配更新。

本页内容包括：

* [Swift 4.1 更新](04_revision_history.md#swift_4_1)
* [Swift 4.0.3 更新](04_revision_history.md#swift_4_0_3)
* [Swift 4.0 更新](04_revision_history.md#swift_4_0)
* [Swift 3.1 更新](04_revision_history.md#swift_3_1)
* [Swift 3.0 更新](04_revision_history.md#swift_3_0)
* [Swift 2.2 更新](04_revision_history.md#swift_2_2)
* [Swift 2.1 更新](04_revision_history.md#swift_2_1)
* [Swift 2.0 更新](04_revision_history.md#swift_2_0)
* [Swift 1.2 更新](04_revision_history.md#swift_1_2)
* [Swift 1.1 更新](04_revision_history.md#swift_1_1)
* [Swift 1.0 更新](04_revision_history.md#swift_1_0)

## Swift 4.1 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2018-03-29</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 4.1&#x3002;</li>
          <li>&#x6DFB;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID574">&#x6709;&#x6761;&#x4EF6;&#x9075;&#x5B88;&#x534F;&#x8BAE;</a>&#x7AE0;&#x8282;&#xFF0C;&#x5176;&#x4E2D;&#x5305;&#x542B;&#x6709;&#x5173;&#x8C03;&#x8282;&#x534F;&#x8BAE;&#x4E00;&#x81F4;&#x6027;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x5728;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID575">&#x5728;&#x5176;&#x5173;&#x8054;&#x7C7B;&#x578B;&#x7EA6;&#x675F;&#x4E2D;&#x4F7F;&#x7528;&#x534F;&#x8BAE;</a>&#x7AE0;&#x8282;&#x6DFB;&#x52A0;&#x4E86;&#x9012;&#x5F52;&#x534F;&#x8BAE;&#x7EA6;&#x675F;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x5728;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID539">&#x6761;&#x4EF6;&#x7F16;&#x8BD1;&#x5757;</a>&#x7AE0;&#x8282;&#x4E2D;&#x6DFB;&#x52A0;&#x6709;&#x5173; <code>canImport()</code> &#x548C; <code>targetEnvironment()</code> &#x5E73;&#x53F0;&#x6761;&#x4EF6;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 4.0.3 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2017-12-04</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 4.0.3&#x3002;</li>
          <li>&#x66F4;&#x65B0; <a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID563">Key-Path &#x8868;&#x8FBE;&#x5F0F;</a>&#xFF0C;&#x73B0;&#x5728;
            key path &#x652F;&#x6301;&#x4E0B;&#x6807;&#x5B50;&#x8DEF;&#x5F84;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 4.0 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2017-09-19</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 4.0&#x3002;</li>
          <li>Added information about exclusive access to memory to the Memory Safety
            chapter.</li>
          <li>Added the Associated Types with a Generic Where Clause section, now that
            you can use generic where clauses to constrain associated types.</li>
          <li>Added information about multiline string literals to the String Literals
            section of the Strings and Characters chapter, and to the String Literals
            section of the Lexical Structure chapter.</li>
          <li>Updated the discussion of the objc attribute in Declaration Attributes,
            now that this attribute is inferred in fewer places.</li>
          <li>Added the Generic Subscripts section, now that subscripts can be generic.</li>
          <li>Updated the discussion in the Protocol Composition section of the Protocols
            chapter, and in the Protocol Composition Type section of the Types chapter,
            now that protocol composition types can contain a superclass requirement.</li>
          <li>Updated the discussion of protocol extensions in Extension Declaration
            now that final isn&#x2019;t allowed in them.</li>
          <li>Added information about preconditions and fatal errors to the Assertions
            and Preconditions section.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 3.1 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2017-03-27</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 3.1&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID553">&#x901A;&#x7528; Where &#x5B50;&#x53E5;&#x6269;&#x5C55;</a>&#xFF0C;&#x5176;&#x4E2D;&#x5305;&#x542B;&#x9700;&#x8981;&#x7684;&#x6269;&#x5C55;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x4E00;&#x4E2A;&#x533A;&#x95F4;&#x8FED;&#x4EE3;&#x7684;&#x4F8B;&#x5B50;&#x5230;
            <a
            href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID121">For-In &#x5FAA;&#x73AF;</a>&#x7AE0;&#x8282;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E00;&#x4E2A;&#x53EF;&#x5931;&#x8D25;&#x6570;&#x503C;&#x8F6C;&#x6362;&#x7684;&#x4F8B;&#x5B50;&#x5230;
            <a
            href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID224">&#x53EF;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;</a>&#x7AE0;&#x8282;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x5173;&#x4E8E;&#x4F7F;&#x7528; Swift &#x8BED;&#x8A00;&#x7248;&#x672C;&#x7684; <code>available</code> &#x7279;&#x6027;&#x4FE1;&#x606F;&#x5230;
            <a
            href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x7279;&#x6027;</a>&#x7AE0;&#x8282;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID449">&#x51FD;&#x6570;&#x7C7B;&#x578B;</a>&#x7AE0;&#x8282;&#x4E2D;&#x7684;&#x63CF;&#x8FF0;&#xFF0C;&#x6CE8;&#x610F;&#x5728;&#x5199;&#x51FD;&#x6570;&#x7C7B;&#x578B;&#x65F6;&#x4E0D;&#x5141;&#x8BB8;&#x4F7F;&#x7528;&#x53C2;&#x6570;&#x6807;&#x7B7E;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID539">&#x6761;&#x4EF6;&#x7F16;&#x8BD1;&#x5757;</a>&#x7AE0;&#x8282;&#x4E2D;&#x7684;
            Swift &#x8BED;&#x8A00;&#x7248;&#x672C;&#x53F7;&#x7684;&#x63CF;&#x8FF0;&#xFF0C;&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x4F7F;&#x7528;&#x53EF;&#x9009;&#x7684;&#x8865;&#x4E01;&#x7248;&#x672C;&#x53F7;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID449">&#x51FD;&#x6570;&#x7C7B;&#x578B;</a>&#x7AE0;&#x8282;&#x7684;&#x63CF;&#x8FF0;&#xFF0C;&#x73B0;&#x5728;
            Swift &#x533A;&#x5206;&#x4E86;&#x91C7;&#x7528;&#x591A;&#x53C2;&#x6570;&#x7684;&#x51FD;&#x6570;&#x548C;&#x91C7;&#x7528;&#x5143;&#x7EC4;&#x7C7B;&#x578B;&#x7684;&#x5355;&#x4E2A;&#x53C2;&#x6570;&#x7684;&#x51FD;&#x6570;&#x3002;</li>
          <li>&#x4ECE;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID383">&#x8868;&#x8FBE;&#x5F0F;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5220;&#x9664;&#x4E86;&#x52A8;&#x6001;&#x8868;&#x8FBE;&#x5F0F;&#x7684;&#x90E8;&#x5206;&#xFF0C;&#x73B0;&#x5728; <code>type(of:)</code> &#x662F;
            Swift &#x6807;&#x51C6;&#x5E93;&#x51FD;&#x6570;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 3.0 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2016-10-27</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 3.0.1&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID48">&#x81EA;&#x52A8;&#x5F15;&#x7528;&#x8BA1;&#x6570;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;
            weak &#x548C; unowned &#x5F15;&#x7528;&#x7684;&#x8BA8;&#x8BBA;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID381">&#x58F0;&#x660E;&#x6807;&#x8BC6;&#x7B26;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x65B0;&#x7684;&#x6807;&#x8BC6;&#x7B26;
            `unowned`&#xFF0C;`unowend(safe)` &#x548C; `unowned(unsafe)` &#x7684;&#x63CF;&#x8FF0;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TypeCasting.html#//apple_ref/doc/uid/TP40014097-CH22-ID342">Any &#x548C; AnyObject &#x7684;&#x7C7B;&#x578B;&#x8F6C;&#x6362;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x4F7F;&#x7528;&#x7C7B;&#x578B;
            `Any` &#x4F5C;&#x4E3A;&#x53EF;&#x9009;&#x503C;&#x7684;&#x63CF;&#x8FF0;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID383">&#x8868;&#x8FBE;&#x5F0F;</a>&#x7AE0;&#x8282;&#xFF0C;&#x628A;&#x62EC;&#x53F7;&#x8868;&#x8FBE;&#x5F0F;&#x548C;&#x5143;&#x7EC4;&#x8868;&#x8FBE;&#x5F0F;&#x7684;&#x63CF;&#x8FF0;&#x5206;&#x5F00;&#x3002;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2016-09-13</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 3.0&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html#//apple_ref/doc/uid/TP40014097-CH10-ID158">&#x51FD;&#x6570;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x51FD;&#x6570;&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x5728;
            <a
            href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x51FD;&#x6570;&#x5B9A;&#x4E49;</a>&#x4E00;&#x8282;&#x4E2D;&#xFF0C;&#x6807;&#x660E;&#x6240;&#x6709;&#x51FD;&#x6570;&#x53C2;&#x6570;&#x9ED8;&#x8BA4;&#x90FD;&#x6709;&#x51FD;&#x6570;&#x6807;&#x7B7E;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID28">&#x9AD8;&#x7EA7;&#x64CD;&#x4F5C;&#x7B26;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x64CD;&#x4F5C;&#x7B26;&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x73B0;&#x5728;&#x4F60;&#x53EF;&#x4EE5;&#x4F5C;&#x4E3A;&#x7C7B;&#x578B;&#x51FD;&#x6570;&#x6765;&#x5B9E;&#x73B0;&#xFF0C;&#x66FF;&#x4EE3;&#x4E4B;&#x524D;&#x7684;&#x5168;&#x5C40;&#x51FD;&#x6570;&#x5B9E;&#x73B0;&#x65B9;&#x5F0F;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID3">&#x8BBF;&#x95EE;&#x63A7;&#x5236;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5BF9;&#x65B0;&#x7684;&#x8BBF;&#x95EE;&#x7EA7;&#x522B;&#x63CF;&#x8FF0;&#x7B26;<code>open</code>&#x548C;<code>fileprivate</code>&#x7684;&#x4FE1;&#x606F;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x51FD;&#x6570;&#x5B9A;&#x4E49;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>inout</code>&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x6807;&#x660E;&#x5B83;&#x653E;&#x5728;&#x53C2;&#x6570;&#x7C7B;&#x578B;&#x7684;&#x524D;&#x9762;&#xFF0C;&#x66FF;&#x4EE3;&#x4E4B;&#x524D;&#x653E;&#x5728;&#x53C2;&#x6570;&#x540D;&#x79F0;&#x524D;&#x9762;&#x7684;&#x65B9;&#x5F0F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x9003;&#x9038;&#x95ED;&#x5305;</a>&#x548C;
            <a
            href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x81EA;&#x52A8;&#x95ED;&#x5305;</a>&#x8FD8;&#x6709;<a href="https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x5C5E;&#x6027;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>@noescape</code>&#x548C;<code>@autoclosure</code>&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x73B0;&#x5728;&#x4ED6;&#x4EEC;&#x662F;&#x7C7B;&#x578B;&#x5C5E;&#x6027;&#xFF0C;&#x800C;&#x4E0D;&#x662F;&#x5B9A;&#x4E49;&#x5C5E;&#x6027;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID28">&#x9AD8;&#x7EA7;&#x64CD;&#x4F5C;&#x7B26;</a>&#x7AE0;&#x8282;&#x4E2D;
            <a
            href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID47">&#x81EA;&#x5B9A;&#x4E49;&#x4E2D;&#x7F00;&#x64CD;&#x4F5C;&#x7B26;&#x7684;&#x4F18;&#x5148;&#x7EA7;</a>&#x4E00;&#x8282;&#x548C;
              <a
              href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID351">&#x5B9A;&#x4E49;</a>&#x7AE0;&#x8282;&#x4E2D;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID550">&#x4F18;&#x5148;&#x7EA7;&#x7EC4;&#x58F0;&#x660E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x64CD;&#x4F5C;&#x7B26;&#x4F18;&#x5148;&#x7EA7;&#x7EC4;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E00;&#x4E9B;&#x8BA8;&#x8BBA;&#xFF1A;&#x4F7F;&#x7528;
            macOS &#x66FF;&#x6362;&#x6389; OS X&#xFF0C; Error &#x66FF;&#x6362;&#x6389;
            ErrorProtocol&#xFF0C;&#x548C;&#x66F4;&#x65B0;&#x4E00;&#x4E9B;&#x534F;&#x8BAE;&#x540D;&#x79F0;&#xFF0C;&#x6BD4;&#x5982;&#x4F7F;&#x7528;
            ExpressibleByStringLiteral &#x66FF;&#x6362;&#x6389; StringLiteralConvertible&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179">&#x6CDB;&#x578B;</a>&#x7AE0;&#x8282;&#x4E2D;
            <a
            href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID192">&#x6CDB;&#x578B; Where &#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x548C;
              <a
              href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/GenericParametersAndArguments.html#//apple_ref/doc/uid/TP40014097-CH37-ID406">&#x6CDB;&#x578B;&#x5F62;&#x53C2;&#x548C;&#x5B9E;&#x53C2;</a>&#x7AE0;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x6CDB;&#x578B;&#x7684;
                where &#x8BED;&#x53E5;&#x5199;&#x5728;&#x4E00;&#x4E2A;&#x58F0;&#x660E;&#x7684;&#x6700;&#x540E;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID546">&#x9003;&#x9038;&#x95ED;&#x5305;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x95ED;&#x5305;&#x9ED8;&#x8BA4;&#x4E3A;&#x975E;&#x9003;&#x9038;&#x7684;&#xFF08;noescaping&#xFF09;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309">&#x57FA;&#x7840;&#x90E8;&#x5206;</a>&#x7AE0;&#x8282;&#x4E2D;
            <a
            href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID333">&#x53EF;&#x9009;&#x7ED1;&#x5B9A;</a>&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID428">&#x8BED;&#x53E5;</a>&#x7AE0;&#x8282;&#x4E2D;
              <a
              href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID432">While &#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728; if&#xFF0C;while
                &#x548C; guard &#x8BED;&#x53E5;&#x4F7F;&#x7528;&#x9017;&#x53F7;&#x5206;&#x9694;&#x6761;&#x4EF6;&#x5217;&#x8868;&#xFF0C;&#x4E0D;&#x9700;&#x8981;&#x4F7F;&#x7528;
                where &#x8BED;&#x53E5;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120">&#x63A7;&#x5236;&#x6D41;</a>&#x7AE0;&#x8282;&#x4E2D;
            <a
            href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID129">Switch</a>&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID428">&#x8BED;&#x53E5;</a>&#x7AE0;&#x8282;&#x4E2D;
              <a
              href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID436">Switch &#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x5173;&#x4E8E; switch cases
                &#x53EF;&#x4EE5;&#x4F7F;&#x7528;&#x591A;&#x6A21;&#x5F0F;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID449">&#x51FD;&#x6570;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x51FD;&#x6570;&#x53C2;&#x6570;&#x6807;&#x7B7E;&#x4E0D;&#x5305;&#x542B;&#x5728;&#x51FD;&#x6570;&#x7C7B;&#x578B;&#x4E2D;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID267">&#x534F;&#x8BAE;</a>&#x7AE0;&#x8282;&#x4E2D;
            <a
            href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID282">&#x534F;&#x8BAE;&#x7EC4;&#x5408;</a>&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID445">&#x7C7B;&#x578B;</a>&#x7AE0;&#x8282;&#x4E2D;
              <a
              href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID454">&#x534F;&#x8BAE;&#x7EC4;&#x5408;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#x5173;&#x4E8E;&#x4F7F;&#x7528;&#x65B0;&#x7684;
                Protocol1 &amp; Protocol2 &#x8BED;&#x6CD5;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID402">&#x52A8;&#x6001;&#x7C7B;&#x578B;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4F7F;&#x7528;&#x65B0;&#x7684;
            type(of:) &#x8868;&#x8FBE;&#x5F0F;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID540">&#x884C;&#x63A7;&#x5236;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4F7F;&#x7528;
            #sourceLocation(file:line:) &#x8868;&#x8FBE;&#x5F0F;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID551">&#x6C38;&#x4E0D;&#x8FD4;&#x56DE;&#x51FD;&#x6570;</a>&#x4E00;&#x8282;&#x4F7F;&#x7528;
            &#x65B0;&#x7684; Never &#x7C7B;&#x578B;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID390">&#x5B57;&#x9762;&#x91CF;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x5173;&#x4E8E;
            playground &#x5B57;&#x9762;&#x91CF;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID545">In-Out &#x53C2;&#x6570;</a>&#x4E00;&#x8282;&#xFF0C;&#x6807;&#x660E;&#x53EA;&#x6709;&#x975E;&#x9003;&#x9038;&#x95ED;&#x5305;&#x80FD;&#x6355;&#x83B7;
            in-out &#x53C2;&#x6570;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html#//apple_ref/doc/uid/TP40014097-CH10-ID169">&#x9ED8;&#x8BA4;&#x53C2;&#x6570;&#x503C;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x9ED8;&#x8BA4;&#x53C2;&#x6570;&#x4E0D;&#x80FD;&#x5728;&#x8C03;&#x7528;&#x65F6;&#x5019;&#x91CD;&#x65B0;&#x6392;&#x5E8F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID347">&#x5C5E;&#x6027;</a>&#x7AE0;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5C5E;&#x6027;&#x53C2;&#x6570;&#x4F7F;&#x7528;&#x5206;&#x53F7;&#x7684;&#x8BF4;&#x660E;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID531">&#x91CD;&#x65B0;&#x629B;&#x51FA;&#x51FD;&#x6570;&#x548C;&#x65B9;&#x6CD5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5728;
            catch &#x4EE3;&#x7801;&#x5757;&#x4E2D;&#x629B;&#x51FA;&#x9519;&#x8BEF;&#x7684;&#x91CD;&#x65B0;&#x629B;&#x51FA;&#x51FD;&#x6570;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID547">Selector &#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x8BBF;&#x95EE;
            Objective-C &#x4E2D; Selector &#x7684; getter &#x548C; setter &#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID361">&#x7C7B;&#x578B;&#x522B;&#x540D;&#x58F0;&#x660E;</a>&#x4E00;&#x8282;&#xFF0C;&#x6807;&#x660E;&#x51FD;&#x6570;&#x7C7B;&#x578B;&#x4F5C;&#x4E3A;&#x53C2;&#x6570;&#x7C7B;&#x578B;&#x5FC5;&#x987B;&#x4F7F;&#x7528;&#x62EC;&#x53F7;&#x5305;&#x88F9;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID449">&#x51FD;&#x6570;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x6CDB;&#x578B;&#x7C7B;&#x578B;&#x522B;&#x540D;&#x548C;&#x5728;&#x534F;&#x8BAE;&#x5185;&#x4F7F;&#x7528;&#x7C7B;&#x578B;&#x522B;&#x540D;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID347">&#x5C5E;&#x6027;</a>&#x7AE0;&#x8282;&#xFF0C;&#x6807;&#x660E;
            @IBAction&#xFF0C;@IBOutlet &#x548C; @NSManaged &#x9690;&#x5F0F;&#x542B;&#x6709;
            @objc &#x5C5E;&#x6027;&#x3002;</li>
          <li>&#x589E;&#x52A0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x5C5E;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;
            @GKInspectable &#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID284">&#x53EF;&#x9009;&#x534F;&#x8BAE;&#x8981;&#x6C42;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x53EA;&#x80FD;&#x5728;&#x4E0E;
            Objective-C &#x4EA4;&#x4E92;&#x7684;&#x4EE3;&#x7801;&#x4E2D;&#x624D;&#x80FD;&#x4F7F;&#x7528;&#x53EF;&#x9009;&#x534F;&#x8BAE;&#x8981;&#x6C42;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x5220;&#x9664;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID362">&#x51FD;&#x6570;&#x58F0;&#x660E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x663E;&#x5F0F;&#x4F7F;&#x7528;
            let &#x5173;&#x952E;&#x5B57;&#x4F5C;&#x4E3A;&#x51FD;&#x6570;&#x53C2;&#x6570;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x5220;&#x9664;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID428">&#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;
            Boolean &#x534F;&#x8BAE;&#x7684;&#x4FE1;&#x606F;&#xFF0C; &#x73B0;&#x5728;&#x8FD9;&#x4E2A;&#x534F;&#x8BAE;&#x5DF2;&#x7ECF;&#x88AB;
            Swift &#x6807;&#x51C6;&#x5E93;&#x5220;&#x9664;&#x3002;</li>
          <li>&#x66F4;&#x6B63;<a href="https://developer.apple.com/library/prerelease/content/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;
            @NSApplicationMain &#x534F;&#x8BAE;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 2.2 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">2016-03-21</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 2.2&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID539">&#x7F16;&#x8BD1;&#x914D;&#x7F6E;&#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5982;&#x4F55;&#x6839;&#x636E;
            Swift &#x7248;&#x672C;&#x8FDB;&#x884C;&#x6761;&#x4EF6;&#x7F16;&#x8BD1;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID400">&#x663E;&#x793A;&#x6210;&#x5458;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5982;&#x4F55;&#x533A;&#x5206;&#x53EA;&#x6709;&#x53C2;&#x6570;&#x540D;&#x4E0D;&#x540C;&#x7684;&#x65B9;&#x6CD5;&#x548C;&#x6784;&#x9020;&#x5668;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID547">&#x9009;&#x62E9;&#x5668;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4E2D;&#x9488;&#x5BF9;
            Objective-C &#x9009;&#x62E9;&#x5668;&#x7684; <code>#selector</code> &#x8BED;&#x6CD5;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID189">&#x5173;&#x8054;&#x7C7B;&#x578B;</a>&#x548C;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID374">&#x534F;&#x8BAE;&#x5173;&#x8054;&#x7C7B;&#x578B;</a>&#x58F0;&#x660E;&#xFF0C;&#x4F7F;&#x7528; <code>associatedtype</code> &#x5173;&#x952E;&#x8BCD;&#x4FEE;&#x6539;&#x4E86;&#x5BF9;&#x4E8E;&#x5173;&#x8054;&#x7C7B;&#x578B;&#x7684;&#x8BA8;&#x8BBA;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID224">&#x53EF;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5F53;&#x6784;&#x9020;&#x5668;&#x5728;&#x5B9E;&#x4F8B;&#x5B8C;&#x5168;&#x521D;&#x59CB;&#x5316;&#x4E4B;&#x524D;&#x8FD4;&#x56DE; <code>nil</code>&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID70">&#x6BD4;&#x8F83;&#x8FD0;&#x7B97;&#x7B26;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x6BD4;&#x8F83;&#x5143;&#x7EC4;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-ID413">&#x5173;&#x952E;&#x5B57;&#x548C;&#x6807;&#x70B9;&#x7B26;&#x53F7;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x4F7F;&#x7528;&#x5173;&#x952E;&#x5B57;&#x4F5C;&#x4E3A;&#x5916;&#x90E8;&#x53C2;&#x6570;&#x540D;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-ID413">&#x58F0;&#x660E;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>@objc</code>&#x7279;&#x6027;&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x5E76;&#x6307;&#x51FA;&#x679A;&#x4E3E;&#xFF08;Enumeration)&#x548C;&#x679A;&#x4E3E;&#x7528;&#x4F8B;(Enumaration
            Case&#xFF09;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-ID418">&#x64CD;&#x4F5C;&#x7B26;</a>&#x4E00;&#x8282;&#x4E2D;&#x5BF9;&#x4E8E;&#x81EA;&#x5B9A;&#x4E49;&#x8FD0;&#x7B97;&#x7B26;&#x7684;&#x8BA8;&#x8BBA;&#x5305;&#x542B;&#x4E86;<code>.</code>&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID531">&#x91CD;&#x65B0;&#x629B;&#x51FA;&#x9519;&#x8BEF;&#x7684;&#x51FD;&#x6570;&#x548C;&#x65B9;&#x6CD5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x91CD;&#x65B0;&#x629B;&#x51FA;&#x9519;&#x8BEF;&#x51FD;&#x6570;&#x4E0D;&#x80FD;&#x76F4;&#x63A5;&#x629B;&#x51FA;&#x9519;&#x8BEF;&#x7684;&#x7B14;&#x8BB0;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html#//apple_ref/doc/uid/TP40014097-CH14-ID262">&#x5C5E;&#x6027;&#x89C2;&#x5BDF;&#x5668;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5F53;&#x4F5C;&#x4E3A;
            in-out &#x53C2;&#x6570;&#x4F20;&#x9012;&#x5C5E;&#x6027;&#x65F6;&#xFF0C;&#x5C5E;&#x6027;&#x89C2;&#x5BDF;&#x5668;&#x7684;&#x8C03;&#x7528;&#x884C;&#x4E3A;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1">Swift &#x521D;&#x89C1;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x9519;&#x8BEF;&#x5904;&#x7406;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID53">&#x5F31;&#x5F15;&#x7528;</a>&#x4E00;&#x8282;&#x4E2D;&#x7684;&#x56FE;&#x7247;&#x7528;&#x4EE5;&#x66F4;&#x6E05;&#x695A;&#x7684;&#x5C55;&#x793A;&#x91CD;&#x65B0;&#x5206;&#x914D;&#x8FC7;&#x7A0B;&#x3002;</li>
          <li>&#x5220;&#x9664;&#x4E86; C &#x8BED;&#x8A00;&#x98CE;&#x683C;&#x7684; <code>for</code> &#x5FAA;&#x73AF;&#xFF0C;<code>++</code> &#x524D;&#x7F00;&#x548C;&#x540E;&#x7F00;&#x8FD0;&#x7B97;&#x7B26;&#xFF0C;&#x4EE5;&#x53CA;<code>--</code> &#x524D;&#x7F00;&#x548C;&#x540E;&#x7F00;&#x8FD0;&#x7B97;&#x7B26;&#x3002;</li>
          <li>&#x5220;&#x9664;&#x4E86;&#x5BF9;&#x53D8;&#x91CF;&#x51FD;&#x6570;&#x53C2;&#x6570;&#x548C;&#x67EF;&#x91CC;&#x5316;&#x51FD;&#x6570;&#x7684;&#x7279;&#x6B8A;&#x8BED;&#x6CD5;&#x7684;&#x8BA8;&#x8BBA;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 2.1 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2015-10-20</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 2.1&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID292">&#x5B57;&#x7B26;&#x4E32;&#x63D2;&#x503C;&#xFF08;String Interprolation)</a>&#x548C;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-ID417">&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;(String Literals&#xFF09;</a>&#x5C0F;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x5B57;&#x7B26;&#x4E32;&#x63D2;&#x503C;&#x53EF;&#x5305;&#x542B;&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x5728;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID546">&#x975E;&#x9003;&#x9038;&#x95ED;&#x5305;&#xFF08;Nonescaping Closures&#xFF09;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E; <code>@noescape</code> &#x5C5E;&#x6027;&#x7684;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x7279;&#x6027;&#xFF08;Declaration Attributes&#xFF09;</a>&#x548C;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID539">&#x7F16;&#x8BD1;&#x914D;&#x7F6E;&#x8BED;&#x53E5;&#xFF08;Build Configuration
              Statement&#xFF09;</a>&#x5C0F;&#x8282;&#x4E2D;&#x4E0E; tvOS &#x76F8;&#x5173;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86; <a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID545">In-Out &#x53C2;&#x6570;&#xFF08;In-Out Parameters&#xFF09;</a>&#x5C0F;&#x8282;&#x4E2D;&#x4E0E;
            in-out &#x53C2;&#x6570;&#x884C;&#x4E3A;&#x76F8;&#x5173;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x5728;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID544">&#x6355;&#x83B7;&#x5217;&#x8868;&#xFF08;Capture Lists&#xFF09;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x6307;&#x5B9A;&#x95ED;&#x5305;&#x6355;&#x83B7;&#x5217;&#x8868;&#x88AB;&#x6355;&#x83B7;&#x65F6;&#x6355;&#x83B7;&#x503C;&#x7684;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;&#x901A;&#x8FC7;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-ID248">&#x53EF;&#x9009;&#x94FE;&#x5F0F;&#x8C03;&#x7528;&#x8BBF;&#x95EE;&#x5C5E;&#x6027;&#xFF08;Accessing Properties Through Optional Chaining&#xFF09;</a>&#x4E00;&#x8282;&#xFF0C;&#x9610;&#x660E;&#x4E86;&#x5982;&#x4F55;&#x901A;&#x8FC7;&#x53EF;&#x9009;&#x94FE;&#x5F0F;&#x8C03;&#x7528;&#x8FDB;&#x884C;&#x8D4B;&#x503C;&#x3002;</li>
          <li>&#x6539;&#x8FDB;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID543">&#x81EA;&#x95ED;&#x5305;&#xFF08;Autoclosure&#xFF09;</a>&#x4E00;&#x8282;&#x4E2D;&#x5BF9;&#x81EA;&#x95ED;&#x5305;&#x7684;&#x8BA8;&#x8BBA;&#x3002;</li>
          <li>&#x5728;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1">Swift &#x521D;&#x89C1;&#xFF08;A Swift Tour&#xFF09;</a>&#x4E00;&#x8282;&#x4E2D;&#x66F4;&#x65B0;&#x4E86;&#x4E00;&#x4E2A;&#x4F7F;&#x7528;<code>??</code>&#x64CD;&#x4F5C;&#x7B26;&#x7684;&#x4F8B;&#x5B50;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 2.0 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2015-09-16</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 2.0&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x5BF9;&#x4E8E;&#x9519;&#x8BEF;&#x5904;&#x7406;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#xFF0C;&#x5305;&#x62EC;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html#//apple_ref/doc/uid/TP40014097-CH42-ID508">&#x9519;&#x8BEF;&#x5904;&#x7406;</a>&#x4E00;&#x7AE0;&#x3001;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID533">Do &#x8BED;&#x53E5;</a>&#x3001;
              <a
              href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID518">Throw &#x8BED;&#x53E5;</a>&#x3001;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID532">Defer &#x8BED;&#x53E5;</a>&#x4EE5;&#x53CA;
                <a
                href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID516">try &#x8FD0;&#x7B97;&#x7B26;</a>&#x7684;&#x591A;&#x4E2A;&#x5C0F;&#x8282;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html#//apple_ref/doc/uid/TP40014097-CH42-ID509">&#x8868;&#x793A;&#x5E76;&#x629B;&#x51FA;&#x9519;&#x8BEF;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x6240;&#x6709;&#x7C7B;&#x578B;&#x5747;&#x53EF;&#x9075;&#x5FAA; <code>ErrorType</code> &#x534F;&#x8BAE;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html#//apple_ref/doc/uid/TP40014097-CH42-ID542">&#x5C06;&#x9519;&#x8BEF;&#x8F6C;&#x6362;&#x6210;&#x53EF;&#x9009;&#x503C;</a>&#x4E00;&#x8282; <code>try?</code> &#x5173;&#x952E;&#x5B57;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html#//apple_ref/doc/uid/TP40014097-CH12-ID145">&#x679A;&#x4E3E;</a>&#x4E00;&#x7AE0;&#x7684;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html#//apple_ref/doc/uid/TP40014097-CH12-ID536">&#x9012;&#x5F52;&#x679A;&#x4E3E;</a>&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID351">&#x58F0;&#x660E;</a>&#x4E00;&#x7AE0;&#x7684;
              <a
              href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID365">&#x4EFB;&#x610F;&#x7C7B;&#x578B;&#x7528;&#x4F8B;&#x7684;&#x679A;&#x4E3E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x9012;&#x5F52;&#x679A;&#x4E3E;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120">&#x63A7;&#x5236;&#x6D41;</a>&#x4E00;&#x7AE0;&#x4E2D;
            a href=&quot;https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID523&quot;&gt;&#x68C0;&#x67E5;
            API &#x53EF;&#x7528;&#x6027;&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID428">&#x8BED;&#x53E5;</a>&#x4E00;&#x7AE0;&#x4E2D;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID522">&#x53EF;&#x7528;&#x6027;&#x6761;&#x4EF6;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;
              API &#x53EF;&#x7528;&#x6027;&#x68C0;&#x67E5;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID120">&#x63A7;&#x5236;&#x6D41;</a>&#x4E00;&#x7AE0;&#x7684;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID525">&#x65E9;&#x671F;&#x9000;&#x51FA;</a>&#x4E00;&#x8282;&#x548C;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID428">&#x8BED;&#x53E5;</a>&#x4E00;&#x7AE0;&#x7684;
              <a
              href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID524">guard &#x8BED;&#x53E5;</a>&#x4E2D;&#x5173;&#x4E8E;&#x65B0; <code>guard</code> &#x8BED;&#x53E5;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID267">&#x534F;&#x8BAE;</a>&#x4E00;&#x7AE0;&#x4E2D;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID521">&#x534F;&#x8BAE;&#x6269;&#x5C55;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x534F;&#x8BAE;&#x6269;&#x5C55;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID3">&#x8BBF;&#x95EE;&#x63A7;&#x5236;</a>&#x4E00;&#x7AE0;&#x4E2D;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID519">&#x5355;&#x5143;&#x6D4B;&#x8BD5; target &#x7684;&#x8BBF;&#x95EE;&#x7EA7;&#x522B;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5355;&#x5143;&#x6D4B;&#x8BD5;&#x7684;&#x8BBF;&#x95EE;&#x63A7;&#x5236;&#x76F8;&#x5173;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Patterns.html#//apple_ref/doc/uid/TP40014097-CH36-ID419">&#x6A21;&#x5F0F;</a>&#x4E00;&#x7AE0;&#x4E2D;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Patterns.html#//apple_ref/doc/uid/TP40014097-CH36-ID520">&#x53EF;&#x9009;&#x6A21;&#x5F0F;</a>&#x4E00;&#x8282;&#x4E2D;&#x7684;&#x65B0;&#x53EF;&#x9009;&#x6A21;&#x5F0F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86; <a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ControlFlow.html#//apple_ref/doc/uid/TP40014097-CH9-ID126">Repeat-While</a> &#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>repeat-while</code>&#x5FAA;&#x73AF;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID285">&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;</a>&#x4E00;&#x7AE0;&#xFF0C;&#x73B0;&#x5728;<code>String</code>&#x5728;
            Swift &#x6807;&#x51C6;&#x5E93;&#x4E2D;&#x4E0D;&#x518D;&#x9075;&#x5FAA;<code>CollectionType</code>&#x534F;&#x8BAE;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID314">&#x6253;&#x5370;&#x5E38;&#x91CF;&#x548C;&#x53D8;&#x91CF;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x65B0;
            Swift &#x6807;&#x51C6;&#x5E93;&#x4E2D;&#x5173;&#x4E8E; <code>print(_:separator:terminator)</code> &#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html#//apple_ref/doc/uid/TP40014097-CH12-ID145">&#x679A;&#x4E3E;</a>&#x4E00;&#x7AE0;&#x4E2D;
            <a
            href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html#//apple_ref/doc/uid/TP40014097-CH12-ID535">&#x539F;&#x59CB;&#x503C;&#x7684;&#x9690;&#x5F0F;&#x8D4B;&#x503C;</a>&#x4E00;&#x8282;&#x548C;
              <a
              href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID351">&#x58F0;&#x660E;</a>&#x4E00;&#x7AE0;&#x7684;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID366">&#x5305;&#x542B;&#x539F;&#x59CB;&#x503C;&#x7C7B;&#x578B;&#x7684;&#x679A;&#x4E3E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5305;&#x542B;<code>String</code>&#x539F;&#x59CB;&#x503C;&#x7684;&#x679A;&#x4E3E;&#x7528;&#x4F8B;&#x7684;&#x884C;&#x4E3A;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID543">&#x81EA;&#x95ED;&#x5305;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>@autoclosure</code>&#x7279;&#x6027;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#xFF0C;&#x5305;&#x62EC;&#x5B83;&#x7684;<code>@autoclosure(escaping)</code>&#x5F62;&#x5F0F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>@avaliable</code>&#x548C;<code>warn_unused_result</code>&#x7279;&#x6027;&#x7684;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID350">&#x7C7B;&#x578B;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>@convention</code>&#x7279;&#x6027;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID333">&#x53EF;&#x9009;&#x7ED1;&#x5B9A;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x4F7F;&#x7528;<code>where</code>&#x5B50;&#x53E5;&#x8FDB;&#x884C;&#x591A;&#x53EF;&#x9009;&#x7ED1;&#x5B9A;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID292">&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5728;&#x7F16;&#x8BD1;&#x65F6;&#x4F7F;&#x7528; <code>+</code> &#x8FD0;&#x7B97;&#x7B26;&#x51ED;&#x501F;&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID455">&#x5143;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5143;&#x7C7B;&#x578B;&#x503C;&#x7684;&#x6BD4;&#x8F83;&#x548C;&#x4F7F;&#x7528;&#x5B83;&#x4EEC;&#x901A;&#x8FC7;&#x6784;&#x9020;&#x5668;&#x8868;&#x8FBE;&#x5F0F;&#x6784;&#x9020;&#x5B9E;&#x4F8B;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID336">&#x65AD;&#x8A00;&#x8C03;&#x8BD5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x7528;&#x6237;&#x5B9A;&#x4E49;&#x65AD;&#x8A00;&#x662F;&#x88AB;&#x8B66;&#x7528;&#x7684;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#xFF0C;&#x5BF9;<code>@NSManaged</code>&#x7279;&#x6027;&#x7684;&#x8BA8;&#x8BBA;&#xFF0C;&#x73B0;&#x5728;&#x8FD9;&#x4E2A;&#x7279;&#x6027;&#x53EF;&#x4EE5;&#x88AB;&#x5E94;&#x7528;&#x5230;&#x4E00;&#x4E2A;&#x786E;&#x5B9A;&#x5B9E;&#x4F8B;&#x65B9;&#x6CD5;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html#//apple_ref/doc/uid/TP40014097-CH10-ID171">&#x53EF;&#x53D8;&#x53C2;&#x6570;</a>&#x4E00;&#x8282;&#xFF0C;&#x73B0;&#x5728;&#x53EF;&#x53D8;&#x53C2;&#x6570;&#x53EF;&#x4EE5;&#x58F0;&#x660E;&#x5728;&#x51FD;&#x6570;&#x53C2;&#x6570;&#x5217;&#x8868;&#x7684;&#x4EFB;&#x610F;&#x4F4D;&#x7F6E;&#x4E2D;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID229">&#x91CD;&#x5199;&#x53EF;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;</a>&#x4E00;&#x8282;&#x4E2D;&#xFF0C;&#x5173;&#x4E8E;&#x975E;&#x53EF;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;&#x76F8;&#x5F53;&#x4E8E;&#x4E00;&#x4E2A;&#x53EF;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;&#x901A;&#x8FC7;&#x7236;&#x7C7B;&#x6784;&#x9020;&#x5668;&#x7684;&#x7ED3;&#x679C;&#x8FDB;&#x884C;&#x5F3A;&#x5236;&#x62C6;&#x5305;&#x7684;&#x76F8;&#x5173;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID365">&#x4EFB;&#x610F;&#x7C7B;&#x578B;&#x7528;&#x4F8B;&#x7684;&#x679A;&#x4E3E;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x679A;&#x4E3E;&#x7528;&#x4F8B;&#x4F5C;&#x4E3A;&#x51FD;&#x6570;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Expressions.html#//apple_ref/doc/uid/TP40014097-CH32-ID399">&#x6784;&#x9020;&#x5668;&#x8868;&#x8FBE;&#x5F0F;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x663E;&#x5F0F;&#x5F15;&#x7528;&#x4E00;&#x4E2A;&#x6784;&#x9020;&#x5668;&#x7684;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID538">&#x7F16;&#x8BD1;&#x63A7;&#x5236;&#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x7F16;&#x8BD1;&#x4FE1;&#x606F;&#x4EE5;&#x53CA;&#x884C;&#x63A7;&#x5236;&#x8BED;&#x53E5;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Types.html#//apple_ref/doc/uid/TP40014097-CH31-ID455">&#x5143;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5982;&#x4F55;&#x4ECE;&#x5143;&#x7C7B;&#x578B;&#x503C;&#x4E2D;&#x6784;&#x9020;&#x7C7B;&#x5B9E;&#x4F8B;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID53">&#x5F31;&#x5F15;&#x7528;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5F31;&#x5F15;&#x7528;&#x4F5C;&#x4E3A;&#x7F13;&#x5B58;&#x7684;&#x663E;&#x5B58;&#x7684;&#x4E0D;&#x8DB3;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID292">&#x7C7B;&#x578B;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#xFF0C;&#x63D0;&#x5230;&#x4E86;&#x5B58;&#x50A8;&#x578B;&#x7279;&#x6027;&#x5176;&#x5B9E;&#x662F;&#x61D2;&#x52A0;&#x8F7D;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html#//apple_ref/doc/uid/TP40014097-CH14-ID264">&#x6355;&#x83B7;&#x7C7B;&#x578B;</a>&#x4E00;&#x8282;&#xFF0C;&#x9610;&#x660E;&#x4E86;&#x53D8;&#x91CF;&#x548C;&#x5E38;&#x91CF;&#x5728;&#x95ED;&#x5305;&#x4E2D;&#x5982;&#x4F55;&#x88AB;&#x6355;&#x83B7;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x58F0;&#x660E;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x7528;&#x4EE5;&#x63CF;&#x8FF0;&#x5982;&#x4F55;&#x5728;&#x7C7B;&#x4E2D;&#x4F7F;&#x7528;<code>@objc</code>&#x5173;&#x952E;&#x5B57;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ErrorHandling.html#//apple_ref/doc/uid/TP40014097-CH42-ID512">&#x9519;&#x8BEF;&#x5904;&#x7406;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x6267;&#x884C;<code>throw</code>&#x8BED;&#x53E5;&#x7684;&#x6027;&#x80FD;&#x7684;&#x8BA8;&#x8BBA;&#x3002;&#x589E;&#x52A0;&#x4E86;
            Do &#x8BED;&#x53E5;&#x4E00;&#x8282;&#x4E2D;&#x76F8;&#x4F3C;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID533">&#x7C7B;&#x578B;&#x7279;&#x6027;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x7C7B;&#x3001;&#x7ED3;&#x6784;&#x4F53;&#x548C;&#x679A;&#x4E3E;&#x7684;&#x5B58;&#x50A8;&#x578B;&#x548C;&#x8BA1;&#x7B97;&#x578B;&#x7279;&#x6027;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Statements.html#//apple_ref/doc/uid/TP40014097-CH33-ID441">Break &#x8BED;&#x53E5;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x5E26;&#x6807;&#x7B7E;&#x7684;
            break &#x8BED;&#x53E5;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Properties.html#//apple_ref/doc/uid/TP40014097-CH14-ID262">&#x5C5E;&#x6027;&#x89C2;&#x5BDF;&#x5668;</a>&#x4E00;&#x8282;&#xFF0C;&#x9610;&#x660E;&#x4E86;<code>willSet</code>&#x548C;<code>didSet</code>&#x89C2;&#x5BDF;&#x5668;&#x7684;&#x884C;&#x4E3A;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-ID5">&#x8BBF;&#x95EE;&#x7EA7;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;<code>private</code>&#x4F5C;&#x7528;&#x57DF;&#x8BBF;&#x95EE;&#x7684;&#x76F8;&#x5173;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID53">&#x5F31;&#x5F15;&#x7528;</a>&#x4E00;&#x8282;&#x4E2D;&#x5173;&#x4E8E;&#x82E5;&#x5E94;&#x7528;&#x5728;&#x5783;&#x573E;&#x56DE;&#x6536;&#x7CFB;&#x7EDF;&#x548C;
            ARC &#x4E4B;&#x95F4;&#x7684;&#x533A;&#x522B;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID295">&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#x4E2D;&#x7279;&#x6B8A;&#x5B57;&#x7B26;</a>&#x4E00;&#x8282;&#x4E2D;&#x5BF9;
            Unicode &#x6807;&#x91CF;&#x66F4;&#x7CBE;&#x786E;&#x7684;&#x5B9A;&#x4E49;&#x3002;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 1.2 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2015-4-8</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 1.2&#x3002;</li>
          <li>Swift &#x73B0;&#x5728;&#x81EA;&#x8EAB;&#x63D0;&#x4F9B;&#x4E86;&#x4E00;&#x4E2A;<code>Set</code>&#x96C6;&#x5408;&#x7C7B;&#x578B;&#xFF0C;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-ID484">&#x96C6;&#x5408;</a>
          </li>
          <li> <code>@autoclosure</code>&#x73B0;&#x5728;&#x662F;&#x4E00;&#x4E2A;&#x53C2;&#x6570;&#x58F0;&#x660E;&#x7684;&#x5C5E;&#x6027;&#xFF0C;&#x800C;&#x4E0D;&#x662F;&#x53C2;&#x6570;&#x7C7B;&#x578B;&#x7684;&#x5C5E;&#x6027;&#x3002;&#x8FD9;&#x91CC;&#x8FD8;&#x6709;&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#x53C2;&#x6570;&#x58F0;&#x660E;&#x5C5E;&#x6027;<code>@noescape</code>&#x3002;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-ID348">&#x5C5E;&#x6027;&#x58F0;&#x660E;</a>
          </li>
          <li>&#x5BF9;&#x4E8E;&#x7C7B;&#x578B;&#x5C5E;&#x6027;&#x548C;&#x65B9;&#x6CD5;&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x4F7F;&#x7528;<code>static</code>&#x5173;&#x952E;&#x5B57;&#x4F5C;&#x4E3A;&#x58F0;&#x660E;&#x63CF;&#x8FF0;&#x7B26;&#xFF0C;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID483">&#x7C7B;&#x578B;&#x53D8;&#x91CF;&#x5C5E;&#x6027;</a>
          </li>
          <li>Swift &#x73B0;&#x5728;&#x5305;&#x542B;&#x4E00;&#x4E2A;<code>as?</code>&#x548C;<code>as!</code>&#x7684;&#x5411;&#x4E0B;&#x53EF;&#x5931;&#x8D25;&#x7C7B;&#x578B;&#x8F6C;&#x6362;&#x8FD0;&#x7B97;&#x7B26;&#x3002;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-ID283">&#x534F;&#x8BAE;&#x9075;&#x5FAA;&#x6027;&#x68C0;&#x67E5;</a>
          </li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#x6307;&#x5BFC;&#x7AE0;&#x8282;&#xFF0C;&#x5B83;&#x662F;&#x5173;&#x4E8E;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID495">&#x5B57;&#x7B26;&#x4E32;&#x7D22;&#x5F15;</a>&#x7684;</li>
          <li>&#x4ECE;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID37">&#x6EA2;&#x51FA;&#x8FD0;&#x7B97;&#x7B26;</a>&#x4E2D;&#x79FB;&#x9664;&#x4E86;&#x6EA2;&#x51FA;&#x9664;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;&amp;/&#xFF09;&#x548C;&#x6C42;&#x4F59;&#x6EA2;&#x51FA;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;&amp;%&#xFF09;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;&#x5E38;&#x91CF;&#x548C;&#x5E38;&#x91CF;&#x5C5E;&#x6027;&#x5728;&#x58F0;&#x660E;&#x548C;&#x6784;&#x9020;&#x65F6;&#x7684;&#x89C4;&#x5219;&#xFF0C;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID355">&#x5E38;&#x91CF;&#x58F0;&#x660E;</a>
          </li>
          <li>&#x66F4;&#x65B0;&#x4E86;&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#x4E2D;
            Unicode &#x6807;&#x91CF;&#x96C6;&#x7684;&#x5B9A;&#x4E49;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-ID295">&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#x4E2D;&#x7684;&#x7279;&#x6B8A;&#x5B57;&#x7B26;</a>
          </li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID73">&#x533A;&#x95F4;&#x8FD0;&#x7B97;&#x7B26;</a>&#x7AE0;&#x8282;&#x6765;&#x63D0;&#x793A;&#x5F53;&#x534A;&#x5F00;&#x533A;&#x95F4;&#x8FD0;&#x7B97;&#x7B26;&#x542B;&#x6709;&#x76F8;&#x540C;&#x7684;&#x8D77;&#x6B62;&#x7D22;&#x5F15;&#x65F6;&#xFF0C;&#x5176;&#x533A;&#x95F4;&#x4E3A;&#x7A7A;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID104">&#x95ED;&#x5305;&#x5F15;&#x7528;&#x7C7B;&#x578B;</a>&#x7AE0;&#x8282;&#x6765;&#x6F84;&#x6E05;&#x5BF9;&#x4E8E;&#x53D8;&#x91CF;&#x7684;&#x6355;&#x83B7;&#x89C4;&#x5219;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-ID38">&#x503C;&#x6EA2;&#x51FA;</a>&#x7AE0;&#x8282;&#x6765;&#x6F84;&#x6E05;&#x6709;&#x7B26;&#x53F7;&#x6574;&#x6570;&#x548C;&#x65E0;&#x7B26;&#x53F7;&#x6574;&#x6570;&#x7684;&#x6EA2;&#x51FA;&#x884C;&#x4E3A;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID369">&#x534F;&#x8BAE;&#x58F0;&#x660E;</a>&#x7AE0;&#x8282;&#x6765;&#x6F84;&#x6E05;&#x534F;&#x8BAE;&#x58F0;&#x660E;&#x65F6;&#x7684;&#x4F5C;&#x7528;&#x57DF;&#x548C;&#x6210;&#x5458;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html#//apple_ref/doc/uid/TP40014097-CH20-ID58">&#x6355;&#x83B7;&#x5217;&#x8868;</a>&#x7AE0;&#x8282;&#x6765;&#x6F84;&#x6E05;&#x5BF9;&#x4E8E;&#x95ED;&#x5305;&#x6355;&#x83B7;&#x5217;&#x8868;&#x4E2D;&#x7684;&#x5F31;&#x5F15;&#x7528;&#x548C;&#x65E0;&#x4E3B;&#x5F15;&#x7528;&#x7684;&#x4F7F;&#x7528;&#x8BED;&#x6CD5;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-ID418">&#x8FD0;&#x7B97;&#x7B26;</a>&#x7AE0;&#x8282;&#x6765;&#x660E;&#x786E;&#x6307;&#x660E;&#x4E00;&#x4E9B;&#x4F8B;&#x5B50;&#x6765;&#x8BF4;&#x660E;&#x81EA;&#x5B9A;&#x4E49;&#x8FD0;&#x7B97;&#x7B26;&#x6240;&#x652F;&#x6301;&#x7684;&#x7279;&#x6027;&#xFF0C;&#x5982;&#x6570;&#x5B66;&#x8FD0;&#x7B97;&#x7B26;&#xFF0C;&#x5404;&#x79CD;&#x7B26;&#x53F7;&#xFF0C;Unicode
            &#x7B26;&#x53F7;&#x5757;&#x7B49;</li>
          <li>&#x5728;&#x51FD;&#x6570;&#x4F5C;&#x7528;&#x57DF;&#x4E2D;&#x7684;&#x5E38;&#x91CF;&#x58F0;&#x660E;&#x65F6;&#x53EF;&#x4EE5;&#x4E0D;&#x88AB;&#x521D;&#x59CB;&#x5316;&#xFF0C;&#x5B83;&#x5FC5;&#x987B;&#x5728;&#x7B2C;&#x4E00;&#x6B21;&#x4F7F;&#x7528;&#x524D;&#x88AB;&#x8D4B;&#x503C;&#x3002;&#x66F4;&#x591A;&#x7684;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-ID355">&#x5E38;&#x91CF;&#x58F0;&#x660E;</a>
          </li>
          <li>&#x5728;&#x6784;&#x9020;&#x5668;&#x4E2D;&#xFF0C;&#x5E38;&#x91CF;&#x5C5E;&#x6027;&#x6709;&#x4E14;&#x4EC5;&#x80FD;&#x88AB;&#x8D4B;&#x503C;&#x4E00;&#x6B21;&#x3002;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID212">&#x5728;&#x6784;&#x9020;&#x8FC7;&#x7A0B;&#x4E2D;&#x7ED9;&#x5E38;&#x91CF;&#x5C5E;&#x6027;&#x8D4B;&#x503C;</a>
          </li>
          <li>&#x591A;&#x4E2A;&#x53EF;&#x9009;&#x7ED1;&#x5B9A;&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x5728;<code>if</code>&#x8BED;&#x53E5;&#x540E;&#x9762;&#x4EE5;&#x9017;&#x53F7;&#x5206;&#x9694;&#x7684;&#x8D4B;&#x503C;&#x5217;&#x8868;&#x7684;&#x65B9;&#x5F0F;&#x51FA;&#x73B0;&#xFF0C;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID333">&#x53EF;&#x9009;&#x7ED1;&#x5B9A;</a>
          </li>
          <li>&#x4E00;&#x4E2A;<a href="04_revision_history.md">&#x53EF;&#x9009;&#x94FE;&#x8868;&#x8FBE;&#x5F0F;</a>&#x5FC5;&#x987B;&#x51FA;&#x73B0;&#x5728;&#x540E;&#x7F00;&#x8868;&#x8FBE;&#x5F0F;&#x4E2D;</li>
          <li>&#x534F;&#x8BAE;&#x7C7B;&#x578B;&#x8F6C;&#x6362;&#x4E0D;&#x518D;&#x5C40;&#x9650;&#x4E8E;<code>@obj</code>&#x4FEE;&#x9970;&#x7684;&#x534F;&#x8BAE;&#x4E86;</li>
          <li>&#x5728;&#x8FD0;&#x884C;&#x65F6;&#x53EF;&#x80FD;&#x4F1A;&#x5931;&#x8D25;&#x7684;&#x7C7B;&#x578B;&#x8F6C;&#x6362;&#x53EF;&#x4EE5;&#x4F7F;&#x7528;<code>as?</code>&#x548C;<code>as!</code>&#x8FD0;&#x7B97;&#x7B26;&#xFF0C;&#x800C;&#x786E;&#x4FDD;&#x4E0D;&#x4F1A;&#x5931;&#x8D25;&#x7684;&#x7C7B;&#x578B;&#x8F6C;&#x6362;&#x73B0;&#x5728;&#x4F7F;&#x7528;<code>as</code>&#x8FD0;&#x7B97;&#x7B26;&#x3002;&#x66F4;&#x591A;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="04_revision_history.md">&#x7C7B;&#x578B;&#x8F6C;&#x6362;&#x8FD0;&#x7B97;&#x7B26;</a>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 1.1 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2014-10-16</td>
      <td style="text-align:left">
        <ul>
          <li>&#x66F4;&#x65B0;&#x81F3; Swift 1.1&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x5173;&#x4E8E;<a href="http://developer.apple.com/library/etc/redirect/xcode/devtools/419f35/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html">&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;&#xFF08;Failable Initializers&#xFF09;</a>&#x7684;&#x5B8C;&#x6574;&#x7AE0;&#x8282;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E86;&#x534F;&#x8BAE;&#x4E2D;&#x5173;&#x4E8E;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;&#x8981;&#x6C42;&#x7684;&#x63CF;&#x8FF0;&#x3002;</li>
          <li>&#x5E38;&#x91CF;&#x548C;&#x53D8;&#x91CF;&#x7684; <code>Any</code> &#x7C7B;&#x578B;&#x73B0;&#x53EF;&#x4EE5;&#x5305;&#x542B;&#x51FD;&#x6570;&#x5B9E;&#x4F8B;&#x3002;&#x66F4;&#x65B0;&#x4E86;&#x5173;&#x4E8E; <code>Any</code> &#x76F8;&#x5173;&#x7684;&#x793A;&#x4F8B;&#x6765;&#x5C55;&#x793A;&#x5982;&#x4F55;&#x5728; <code>switch</code> &#x8BED;&#x53E5;&#x4E2D;&#x5982;&#x4F55;&#x68C0;&#x67E5;&#x5E76;&#x8F6C;&#x6362;&#x5230;&#x4E00;&#x4E2A;&#x51FD;&#x6570;&#x7C7B;&#x578B;&#x3002;</li>
          <li>&#x5E26;&#x6709;&#x539F;&#x59CB;&#x503C;&#x7684;&#x679A;&#x4E3E;&#x7C7B;&#x578B;&#x589E;&#x52A0;&#x4E86;&#x4E00;&#x4E2A;<code>rawValue</code>&#x5C5E;&#x6027;&#x66FF;&#x4EE3;<code>toRaw()</code>&#x65B9;&#x6CD5;&#xFF0C;&#x540C;&#x65F6;&#x4F7F;&#x7528;&#x4E86;&#x4E00;&#x4E2A;&#x4EE5;<code>rawValue</code>&#x4E3A;&#x53C2;&#x6570;&#x7684;&#x5931;&#x8D25;&#x6784;&#x9020;&#x5668;&#x6765;&#x66FF;&#x4EE3;<code>fromRaw()</code>&#x65B9;&#x6CD5;&#x3002;&#x66F4;&#x591A;&#x7684;&#x4FE1;&#x606F;&#xFF0C;&#x8BF7;&#x770B;
            <a
            href="http://developer.apple.com/library/etc/redirect/xcode/devtools/419f35/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html">&#x539F;&#x59CB;&#x503C;&#xFF08;Raw Values&#xFF09;</a>&#x548C;<a href="http://developer.apple.com/library/etc/redirect/xcode/devtools/419f35/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html">&#x5E26;&#x539F;&#x59CB;&#x503C;&#x7684;&#x679A;&#x4E3E;&#x7C7B;&#x578B;&#xFF08;Enumerations with Cases of a Raw-Value Type&#xFF09;</a>&#x90E8;&#x5206;&#x3002;</li>
          <li>&#x81EA;&#x5B9A;&#x4E49;&#x8FD0;&#x7B97;&#x7B26;&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x5305;&#x542B;
            `?` &#x5B57;&#x7B26;&#xFF0C;&#x66F4;&#x65B0;&#x7684;<a href="http://developer.apple.com/library/etc/redirect/xcode/devtools/419f35/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html">&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Operators&#xFF09;</a>&#x7AE0;&#x8282;&#x63CF;&#x8FF0;&#x4E86;&#x6539;&#x8FDB;&#x540E;&#x7684;&#x89C4;&#x5219;&#xFF0C;&#x5E76;&#x4E14;&#x4ECE;
            <a
            href="http://developer.apple.com/library/etc/redirect/xcode/devtools/419f35/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html">&#x81EA;&#x5B9A;&#x4E49;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Custom Operators&#xFF09;</a>&#x7AE0;&#x8282;&#x5220;&#x9664;&#x4E86;&#x91CD;&#x590D;&#x7684;&#x8FD0;&#x7B97;&#x7B26;&#x6709;&#x6548;&#x5B57;&#x7B26;&#x96C6;&#x5408;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Swift 1.0 更新

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53D1;&#x5E03;&#x65E5;&#x671F;</th>
      <th style="text-align:left">&#x8BED;&#x6CD5;&#x53D8;&#x66F4;&#x8BB0;&#x5F55;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2014-08-18</td>
      <td style="text-align:left">
        <ul>
          <li>&#x53D1;&#x5E03;&#x65B0;&#x7684;&#x6587;&#x6863;&#x7528;&#x4EE5;&#x8BE6;&#x8FF0;
            Swift 1.0&#xFF0C;&#x82F9;&#x679C;&#x516C;&#x53F8;&#x9488;&#x5BF9; iOS &#x548C;
            OS X &#x5E94;&#x7528;&#x7684;&#x5168;&#x65B0;&#x5F00;&#x53D1;&#x8BED;&#x8A00;&#x3002;</li>
          <li>&#x5728;&#x7AE0;&#x8282;&#x534F;&#x8BAE;&#x4E2D;&#xFF0C;&#x589E;&#x52A0;&#x65B0;&#x7684;&#x5C0F;&#x8282;&#xFF1A;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-XID_397">&#x5BF9;&#x6784;&#x9020;&#x5668;&#x7684;&#x89C4;&#x5B9A;&#xFF08;Initializer
              Requirements&#xFF09;</a>
          </li>
          <li>&#x5728;&#x7AE0;&#x8282;&#x534F;&#x8BAE;&#x4E2D;&#xFF0C;&#x589E;&#x52A0;&#x65B0;&#x7684;&#x5C0F;&#x8282;&#xFF1A;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Protocols.html#//apple_ref/doc/uid/TP40014097-CH25-XID_409">&#x7C7B;&#x4E13;&#x5C5E;&#x534F;&#x8BAE;&#xFF08;class-only protocols&#xFF09;</a>
          </li>
          <li> <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-XID_494">&#x65AD;&#x8A00;&#xFF08;assertions&#xFF09;</a>&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x4F7F;&#x7528;&#x5B57;&#x7B26;&#x4E32;&#x5185;&#x63D2;&#x8BED;&#x6CD5;&#xFF0C;&#x5E76;&#x5220;&#x9664;&#x4E86;&#x6587;&#x6863;&#x4E2D;&#x6709;&#x51B2;&#x7A81;&#x7684;&#x6CE8;&#x91CA;</li>
          <li>&#x66F4;&#x65B0;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_428">&#x8FDE;&#x63A5;&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;&#xFF08;Concatenating Strings and Characters&#xFF09;</a>&#x5C0F;&#x8282;&#x6765;&#x8BF4;&#x660E;&#x4E00;&#x4E2A;&#x4E8B;&#x5B9E;&#xFF0C;&#x90A3;&#x5C31;&#x662F;&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;&#x4E0D;&#x80FD;&#x518D;&#x7528;<code>+</code>&#x53F7;&#x8FD0;&#x7B97;&#x7B26;&#x6216;&#x8005;&#x590D;&#x5408;&#x52A0;&#x6CD5;&#x8FD0;&#x7B97;&#x7B26;<code>+=</code>&#x76F8;&#x4E92;&#x8FDE;&#x63A5;&#xFF0C;&#x8FD9;&#x4E24;&#x79CD;&#x8FD0;&#x7B97;&#x7B26;&#x73B0;&#x5728;&#x53EA;&#x80FD;&#x7528;&#x4E8E;&#x5B57;&#x7B26;&#x4E32;&#x4E4B;&#x95F4;&#x76F8;&#x8FDE;&#x3002;&#x8BF7;&#x4F7F;&#x7528;<code>String</code>&#x7C7B;&#x578B;&#x7684;<code>append</code>&#x65B9;&#x6CD5;&#x5728;&#x4E00;&#x4E2A;&#x5B57;&#x7B26;&#x4E32;&#x7684;&#x5C3E;&#x90E8;&#x589E;&#x52A0;&#x5355;&#x4E2A;&#x5B57;&#x7B26;</li>
          <li>&#x5728;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Attributes.html#//apple_ref/doc/uid/TP40014097-CH35-XID_516">&#x58F0;&#x660E;&#x7279;&#x6027;&#xFF08;Declaration Attributes&#xFF09;</a>&#x7AE0;&#x8282;&#x589E;&#x52A0;&#x4E86;&#x5173;&#x4E8E;<code>availability</code>&#x7279;&#x6027;&#x7684;&#x4E00;&#x4E9B;&#x4FE1;&#x606F;</li>
          <li> <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-XID_478">&#x53EF;&#x9009;&#x7C7B;&#x578B;&#xFF08;Optionals&#xFF09;</a> &#x82E5;&#x6709;&#x503C;&#x65F6;&#xFF0C;&#x4E0D;&#x518D;&#x9690;&#x5F0F;&#x7684;&#x8F6C;&#x6362;&#x4E3A; <code>true</code>&#xFF0C;&#x540C;&#x6837;&#xFF0C;&#x82E5;&#x65E0;&#x503C;&#x65F6;&#xFF0C;&#x4E5F;&#x4E0D;&#x518D;&#x9690;&#x5F0F;&#x7684;&#x8F6C;&#x6362;&#x4E3A; <code>false</code>&#xFF0C;&#x8FD9;&#x662F;&#x4E3A;&#x4E86;&#x907F;&#x514D;&#x5728;&#x5224;&#x522B;
            optional <code>Bool</code> &#x7684;&#x503C;&#x65F6;&#x4EA7;&#x751F;&#x56F0;&#x60D1;&#x3002;
            &#x66FF;&#x4EE3;&#x7684;&#x65B9;&#x6848;&#x662F;&#xFF0C;&#x7528;<code>==</code> &#x6216; <code>!=</code> &#x8FD0;&#x7B97;&#x7B26;&#x663E;&#x5F0F;&#x5730;&#x53BB;&#x5224;&#x65AD;
            Optinal &#x662F;&#x5426;&#x662F; <code>nil</code>&#xFF0C;&#x4EE5;&#x786E;&#x8BA4;&#x5176;&#x662F;&#x5426;&#x5305;&#x542B;&#x503C;&#x3002;</li>
          <li>Swift &#x65B0;&#x589E;&#x4E86;&#x4E00;&#x4E2A; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-XID_124">Nil &#x5408;&#x5E76;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Nil Coalescing Operator&#xFF09;</a> (<code>a ?? b</code>),
            &#x8BE5;&#x8868;&#x8FBE;&#x5F0F;&#x4E2D;&#xFF0C;&#x5982;&#x679C; Optional <code>a</code>&#x7684;&#x503C;&#x5B58;&#x5728;&#xFF0C;&#x5219;&#x53D6;&#x5F97;&#x5B83;&#x5E76;&#x8FD4;&#x56DE;&#xFF0C;&#x82E5;
            Optional <code>a</code>&#x4E3A;<code>nil</code>&#xFF0C;&#x5219;&#x8FD4;&#x56DE;&#x9ED8;&#x8BA4;&#x503C; <code>b</code>
          </li>
          <li>&#x66F4;&#x65B0;&#x548C;&#x6269;&#x5C55; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_434">&#x5B57;&#x7B26;&#x4E32;&#x7684;&#x6BD4;&#x8F83;&#xFF08;Comparing Strings&#xFF09;</a> &#x7AE0;&#x8282;&#xFF0C;&#x7528;&#x4EE5;&#x53CD;&#x6620;&#x548C;&#x5C55;&#x793A;&apos;&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;&#x7684;&#x6BD4;&#x8F83;&apos;&#xFF0C;&#x4EE5;&#x53CA;&apos;&#x524D;&#x7F00;&#xFF08;prefix&#xFF09;/&#x540E;&#x7F00;&#xFF08;postfix&#xFF09;&#x6BD4;&#x8F83;&apos;&#x90FD;&#x5F00;&#x59CB;&#x57FA;&#x4E8E;&#x6269;&#x5C55;&#x5B57;&#x7B26;&#x96C6;&#xFF08;extended
            grapheme clusters&#xFF09;&#x89C4;&#x8303;&#x7684;&#x7B49;&#x4EF7;&#x6BD4;&#x8F83;&#x3002;</li>
          <li>&#x73B0;&#x5728;&#xFF0C;&#x4F60;&#x53EF;&#x4EE5;&#x901A;&#x8FC7; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-XID_356">&#x53EF;&#x9009;&#x94FE;&#xFF08;Optional Chaining&#xFF09;</a>&#x6765;&#xFF1A;&#x7ED9;&#x5C5E;&#x6027;&#x8BBE;&#x503C;&#xFF0C;&#x5C06;&#x5176;&#x8D4B;&#x7ED9;&#x4E00;&#x4E2A;&#x4E0B;&#x6807;&#x811A;&#x6CE8;&#xFF08;subscript&#xFF09;;
            &#x6216;&#x8C03;&#x7528;&#x4E00;&#x4E2A;&#x53D8;&#x5F02;&#xFF08;mutating&#xFF09;&#x65B9;&#x6CD5;&#x6216;&#x8FD0;&#x7B97;&#x7B26;&#x3002;&#x5BF9;&#x6B64;&#xFF0C;&#x7AE0;&#x8282;&#x2014;&#x2014;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-XID_364">&#x901A;&#x8FC7;&#x53EF;&#x9009;&#x94FE;&#x8BBF;&#x95EE;&#x5C5E;&#x6027;&#xFF08;Accessing
              Properties Through Optional Chaining&#xFF09;</a>&#x7684;&#x5185;&#x5BB9;&#x5DF2;&#x7ECF;&#x88AB;&#x76F8;&#x5E94;&#x7684;&#x66F4;&#x65B0;&#x3002;&#x800C;&#x7AE0;&#x8282;&#x2014;&#x2014;
              <a
              href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-XID_361">&#x901A;&#x8FC7;&#x53EF;&#x9009;&#x94FE;&#x8C03;&#x7528;&#x65B9;&#x6CD5;&#xFF08;Calling
                Methods Through Optional Chaining</a>&#x4E2D;&#xFF0C;&#x5173;&#x4E8E;&#x68C0;&#x67E5;&#x65B9;&#x6CD5;&#x8C03;&#x7528;&#x662F;&#x5426;&#x6210;&#x529F;&#x7684;&#x4F8B;&#x5B50;&#xFF0C;&#x5DF2;&#x88AB;&#x6269;&#x5C55;&#x4E3A;&#x5C55;&#x793A;&#x5982;&#x4F55;&#x68C0;&#x67E5;&#x4E00;&#x4E2A;&#x5C5E;&#x6027;&#x662F;&#x5426;&#x88AB;&#x8BBE;&#x503C;&#x6210;&#x529F;&#x3002;</li>
          <li>&#x5728;&#x7AE0;&#x8282;&#x53EF;&#x9009;&#x94FE;&#x4E2D;&#xFF0C;&#x589E;&#x52A0;&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#x5C0F;&#x8282;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/OptionalChaining.html#//apple_ref/doc/uid/TP40014097-CH21-XID_364">&#x8BBF;&#x95EE;&#x53EF;&#x9009;&#x7C7B;&#x578B;&#x7684;&#x4E0B;&#x6807;&#x811A;&#x6CE8;&#xFF08;Accessing
              Subscripts of Optional Type&#xFF09;</a>
          </li>
          <li>&#x66F4;&#x65B0;&#x7AE0;&#x8282; <a href="../chapter2/04_collection_types.md#&#x8BBF;&#x95EE;&#x548C;&#x4FEE;&#x6539;&#x6570;&#x7EC4;">&#x8BBF;&#x95EE;&#x548C;&#x4FEE;&#x6539;&#x6570;&#x7EC4;&#xFF08;Accessing and Modifying an Array&#xFF09;</a> &#x4EE5;&#x6807;&#x793A;&#xFF1A;&#x4ECE;&#x8BE5;&#x7248;&#x672C;&#x8D77;&#xFF0C;&#x4E0D;&#x80FD;&#x518D;&#x901A;&#x8FC7;<code>+=</code> &#x8FD0;&#x7B97;&#x7B26;&#x7ED9;&#x4E00;&#x4E2A;&#x6570;&#x7EC4;&#x6DFB;&#x52A0;&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#x9879;&#x3002;&#x3002;
            &#x5BF9;&#x5E94;&#x7684;&#x66FF;&#x4EE3;&#x65B9;&#x6848;&#x662F;&#xFF0C;&#x4F7F;<code>append</code> &#x65B9;&#x6CD5;&#xFF0C;&#x6216;&#x8005;&#x901A;&#x8FC7;<code>+=</code>&#x8FD0;&#x7B97;&#x7B26;&#x6765;&#x6DFB;&#x52A0;&#x4E00;&#x4E2A;<b>&#x53EA;&#x6709;&#x4E00;&#x4E2A;&#x9879;&#x7684;&#x6570;&#x7EC4;</b>&#xFF08;single-item
            Array&#xFF09;&#x3002;</li>
          <li>&#x6DFB;&#x52A0;&#x4E86;&#x4E00;&#x4E2A;&#x63D0;&#x793A;&#xFF1A;&#x5728;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-XID_126">&#x8303;&#x56F4;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Range Operators&#xFF09;</a>&#x4E2D;&#xFF0C;&#x6BD4;&#x5982;&#xFF0C; <code>a...b</code> &#x548C; <code>a..&lt;b</code> &#xFF0C;&#x8D77;&#x59CB;&#x503C;<code>a</code>&#x4E0D;&#x80FD;&#x5927;&#x4E8E;&#x7ED3;&#x675F;&#x503C;<code>b</code>.</li>
          <li>&#x91CD;&#x5199;&#x4E86;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Inheritance.html#//apple_ref/doc/uid/TP40014097-CH17-XID_293">&#x7EE7;&#x627F;&#xFF08;Inheritance&#xFF09;</a> &#x8FD9;&#x4E00;&#x7AE0;&#xFF1A;&#x5220;&#x9664;&#x4E86;&#x672C;&#x7AE0;&#x4E2D;&#x5173;&#x4E8E;&#x6784;&#x9020;&#x5668;&#x91CD;&#x5199;&#x7684;&#x4ECB;&#x7ECD;&#x6027;&#x62A5;&#x9053;&#xFF1B;&#x8F6C;&#x800C;&#x5C06;&#x66F4;&#x591A;&#x7684;&#x6CE8;&#x610F;&#x529B;&#x653E;&#x5230;&#x65B0;&#x589E;&#x7684;&#x90E8;&#x5206;&#x2014;&#x2014;&#x5B50;&#x7C7B;&#x7684;&#x65B0;&#x529F;&#x80FD;&#xFF0C;&#x4EE5;&#x53CA;&#x5982;&#x4F55;&#x901A;&#x8FC7;&#x91CD;&#x5199;&#xFF08;overrides&#xFF09;&#x4FEE;&#x6539;&#x5DF2;&#x6709;&#x7684;&#x529F;&#x80FD;&#x3002;&#x53E6;&#x5916;&#xFF0C;&#x5C0F;&#x8282;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Inheritance.html#//apple_ref/doc/uid/TP40014097-CH17-XID_301">&#x91CD;&#x5199;&#x5C5E;&#x6027;&#x7684; Getters &#x548C; Setters&#xFF08;Overriding
              Property Getters and Setters&#xFF09;</a>&#x4E2D;&#x7684;&#x4F8B;&#x5B50;&#x5DF2;&#x7ECF;&#x88AB;&#x66FF;&#x6362;&#x4E3A;&#x5C55;&#x793A;&#x5982;&#x4F55;&#x91CD;&#x5199;&#x4E00;&#x4E2A; <code>description</code> &#x5C5E;&#x6027;&#x3002;
              (&#x800C;&#x5173;&#x4E8E;&#x5982;&#x4F55;&#x5728;&#x5B50;&#x7C7B;&#x7684;&#x6784;&#x9020;&#x5668;&#x4E2D;&#x4FEE;&#x6539;&#x7EE7;&#x627F;&#x5C5E;&#x6027;&#x7684;&#x9ED8;&#x8BA4;&#x503C;&#x7684;&#x4F8B;&#x5B50;&#xFF0C;&#x5DF2;&#x7ECF;&#x88AB;&#x79FB;&#x5230;
              <a
              href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Inheritance.html#//apple_ref/doc/uid/TP40014097-CH17-XID_293">&#x6784;&#x9020;&#x8FC7;&#x7A0B;&#xFF08;Initialization&#xFF09;</a>&#x8FD9;&#x4E00;&#x7AE0;&#x3002;)</li>
          <li>&#x66F4;&#x65B0;&#x4E86; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-XID_331">&#x6784;&#x9020;&#x5668;&#x7684;&#x7EE7;&#x627F;&#x4E0E;&#x91CD;&#x5199;&#xFF08;Initializer Inheritance and Overriding&#xFF09;</a> &#x5C0F;&#x8282;&#x4EE5;&#x6807;&#x793A;&#xFF1A;
            &#x91CD;&#x5199;&#x4E00;&#x4E2A;&#x7279;&#x5B9A;&#x7684;&#x6784;&#x9020;&#x5668;&#x5FC5;&#x987B;&#x4F7F;&#x7528; <code>override</code> &#x4FEE;&#x9970;&#x7B26;&#x3002;</li>
          <li>&#x66F4;&#x65B0; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-XID_339">Required &#x6784;&#x9020;&#x5668;&#xFF08;Required Initializers&#xFF09;</a> &#x5C0F;&#x8282;&#x4EE5;&#x6807;&#x793A;&#xFF1A;<code>required</code> &#x4FEE;&#x9970;&#x7B26;&#x73B0;&#x5728;&#x9700;&#x8981;&#x51FA;&#x73B0;&#x5728;&#x6240;&#x6709;&#x5B50;&#x7C7B;&#x7684;
            required &#x6784;&#x9020;&#x5668;&#x7684;&#x58F0;&#x660E;&#x4E2D;&#xFF0C;&#x800C;
            required &#x6784;&#x9020;&#x5668;&#x7684;&#x5B9E;&#x73B0;&#xFF0C;&#x73B0;&#x5728;&#x53EF;&#x4EE5;&#x4EC5;&#x4ECE;&#x7236;&#x7C7B;&#x81EA;&#x52A8;&#x7EE7;&#x627F;&#x3002;</li>
          <li>&#x4E2D;&#x7F6E;&#xFF08;Infix&#xFF09;&#x7684; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_80">&#x8FD0;&#x7B97;&#x7B26;&#x51FD;&#x6570;&#xFF08;Operator Functions&#xFF09;</a> &#x4E0D;&#x518D;&#x9700;&#x8981;<code>@infix</code> &#x5C5E;&#x6027;&#x3002;</li>
          <li> <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/RevisionHistory.html#//apple_ref/doc/uid/TP40014097-CH40-XID_1631">&#x524D;&#x7F6E;&#x548C;&#x540E;&#x7F6E;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Prefix and Postfix Operators&#xFF09;</a>&#x7684;<code>@prefix</code> &#x548C; <code>@postfix</code> &#x5C5E;&#x6027;&#xFF0C;&#x5DF2;&#x53D8;&#x66F4;&#x4E3A; <code>prefix</code> &#x548C; <code>postfix</code> &#x58F0;&#x660E;&#x4FEE;&#x9970;&#x7B26;&#xFF08;declaration
            modifiers&#xFF09;&#x3002;</li>
          <li>&#x589E;&#x52A0;&#x4E00;&#x6761;&#x6CE8;&#x89E3;&#xFF1A;&#x5F53; Prefix
            &#x548C; postfix &#x8FD0;&#x7B97;&#x7B26;&#x88AB;&#x4F5C;&#x7528;&#x4E8E;&#x540C;&#x4E00;&#x4E2A;&#x64CD;&#x4F5C;&#x6570;&#x65F6;&#xFF0C;&#x5173;&#x4E8E;
            <a
            href="https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter1/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_81">&#x524D;&#x7F6E;&#x548C;&#x540E;&#x7F6E;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Prefix
              and Postfix Operators&#xFF09;</a>&#x7684;&#x987A;&#x5E8F;&#xFF08;postfix
              &#x8FD0;&#x7B97;&#x7B26;&#x4F1A;&#x5148;&#x88AB;&#x6267;&#x884C;&#xFF09;</li>
          <li>&#x5728;&#x8FD0;&#x7B97;&#x7B26;&#x51FD;&#x6570;&#xFF08;Operator functions&#xFF09;&#x4E2D;&#xFF0C;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_82">&#x7EC4;&#x5408;&#x8D4B;&#x503C;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Compound
              Assignment Operators&#xFF09;</a>&#x4E0D;&#x518D;&#x4F7F;&#x7528; <code>@assignment</code> &#x5C5E;&#x6027;&#x6765;&#x5B9A;&#x4E49;&#x51FD;&#x6570;&#x3002;</li>
          <li>&#x5728;&#x8FD9;&#x4E2A;&#x7248;&#x672C;&#x4E2D;&#xFF0C;&#x5728;&#x5B9A;&#x4E49;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_85">&#x81EA;&#x5B9A;&#x4E49;&#x64CD;&#x4F5C;&#x7B26;&#xFF08;Custom Operators&#xFF09;</a>&#x65F6;&#xFF0C;<b>&#x4FEE;&#x9970;&#x7B26;&#xFF08;Modifiers&#xFF09;&#x7684;&#x51FA;&#x73B0;&#x987A;&#x5E8F;&#x53D1;&#x751F;&#x53D8;&#x5316;</b>&#x3002;&#x6BD4;&#x5982;&#xFF0C;
              &#x73B0;&#x5728;&#xFF0C;&#x4F60;&#x8BE5;&#x7F16;&#x5199; <code>prefix operator</code>&#xFF0C;
              &#x800C;&#x4E0D;&#x662F; <code>operator prefix</code>.</li>
          <li>&#x589E;&#x52A0;&#x4FE1;&#x606F;&#xFF1A;&#x5173;&#x4E8E;<code>dynamic</code> &#x58F0;&#x660E;&#x4FEE;&#x9970;&#x7B26;&#xFF08;declaration
            modifier&#xFF09;&#xFF0C;&#x4E8E;&#x7AE0;&#x8282; <a href="https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter1/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-XID_705">&#x58F0;&#x660E;&#x4FEE;&#x9970;&#x7B26;&#xFF08;Declaration Modifiers&#xFF09;</a>.</li>
          <li>&#x589E;&#x52A0;&#x4FE1;&#x606F;&#xFF1A;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_886">&#x5B57;&#x9762;&#x91CF; Literals</a> &#x7684;&#x7C7B;&#x578B;&#x63A8;&#x5BFC;&#xFF08;type
            inference&#xFF09;</li>
          <li>&#x4E3A;&#x7AE0;&#x8282;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-XID_597">Curried Functions</a>&#x6DFB;&#x52A0;&#x4E86;&#x66F4;&#x591A;&#x7684;&#x4FE1;&#x606F;&#x3002;</li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html#//apple_ref/doc/uid/TP40014097-CH41-XID_29">&#x6743;&#x9650;&#x63A7;&#x5236;&#xFF08;Access Control&#xFF09;</a>.</li>
          <li>&#x66F4;&#x65B0;&#x4E86;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_413">&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;&#xFF08;Strings and Characters&#xFF09;</a> &#x7528;&#x4EE5;&#x8868;&#x660E;&#xFF0C;&#x5728;
            Swift &#x4E2D;&#xFF0C;<code>Character</code> &#x7C7B;&#x578B;&#x73B0;&#x5728;&#x4EE3;&#x8868;&#x7684;&#x662F;&#x6269;&#x5C55;&#x5B57;&#x7B26;&#x96C6;&#xFF08;extended
            grapheme cluster&#xFF09;&#x4E2D;&#x7684;&#x4E00;&#x4E2A; Unicode&#xFF0C;&#x4E3A;&#x6B64;&#xFF0C;&#x65B0;&#x589E;&#x4E86;&#x5C0F;&#x8282;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_431">Extended Grapheme Clusters</a>&#x3002;&#x540C;&#x65F6;&#xFF0C;&#x4E3A;&#x5C0F;&#x8282;
              <a
              href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_428">Unicode &#x6807;&#x91CF;&#xFF08;Unicode Scalars&#xFF09;</a>&#x548C;
                <a
                href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_434">&#x5B57;&#x7B26;&#x4E32;&#x6BD4;&#x8F83;&#xFF08;Comparing Strings&#xFF09;</a>&#x589E;&#x52A0;&#x4E86;&#x66F4;&#x591A;&#x5185;&#x5BB9;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x7AE0;&#x8282;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_856">&#x5B57;&#x7B26;&#x4E32;&#x5B57;&#x9762;&#x91CF;&#xFF08;String Literals&#xFF09;</a>&#xFF1A;&#x5728;&#x4E00;&#x4E2A;&#x5B57;&#x7B26;&#x4E32;&#x4E2D;&#xFF0C;Unicode
            &#x6807;&#x91CF;&#xFF08;Unicode scalars&#xFF09; &#x4EE5; <code>\u{n}</code>&#x7684;&#x5F62;&#x5F0F;&#x6765;&#x8868;&#x793A;&#xFF0C;<code>n</code> &#x662F;&#x4E00;&#x4E2A;&#x6700;&#x5927;&#x53EF;&#x4EE5;&#x6709;8&#x4F4D;&#x7684;16&#x8FDB;&#x5236;&#x6570;&#xFF08;hexadecimal
            digits&#xFF09;</li>
          <li> <code>NSString</code>  <code>length</code> &#x5C5E;&#x6027;&#x5DF2;&#x88AB;&#x6620;&#x5C04;&#x5230;
            Swift &#x7684;&#x5185;&#x5EFA; <code>String</code>&#x7C7B;&#x578B;&#x3002;&#xFF08;&#x6CE8;&#x610F;&#xFF0C;&#x8FD9;&#x4E24;&#x5C5E;&#x6027;&#x7684;&#x7C7B;&#x578B;&#x662F;<code>utf16Count</code>,&#x800C;&#x975E; <code>utf16count</code>&#xFF09;&#x3002;</li>
          <li>Swift &#x7684;&#x5185;&#x5EFA; <code>String</code> &#x7C7B;&#x578B;&#x4E0D;&#x518D;&#x62E5;&#x6709; <code>uppercaseString</code> &#x548C; <code>lowercaseString</code> &#x5C5E;&#x6027;&#x3002;&#x5176;&#x5BF9;&#x5E94;&#x90E8;&#x5206;&#x5728;&#x7AE0;&#x8282;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_413">&#x5B57;&#x7B26;&#x4E32;&#x548C;&#x5B57;&#x7B26;&#xFF08;Strings and Characters&#xFF09;</a>&#x5DF2;&#x7ECF;&#x88AB;&#x5220;&#x9664;&#xFF0C;&#x5E76;&#x4E14;&#x5404;&#x79CD;&#x5BF9;&#x5E94;&#x7684;&#x4EE3;&#x7801;&#x7528;&#x4F8B;&#x4E5F;&#x5DF2;&#x88AB;&#x66F4;&#x65B0;&#x3002;</li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-XID_315">&#x6CA1;&#x6709;&#x5916;&#x90E8;&#x540D;&#x7684;&#x6784;&#x9020;&#x5668;&#x53C2;&#x6570;&#xFF08;Initializer Parameters Without External Names&#xFF09;</a>.</li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-XID_339">Required &#x6784;&#x9020;&#x5668;&#xFF08;Required Initializers&#xFF09;</a>.</li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Functions.html#//apple_ref/doc/uid/TP40014097-CH10-XID_252">&#x53EF;&#x9009;&#x5143;&#x7956;&#xFF08;&#x51FD;&#x6570;&#xFF09;&#x8FD4;&#x56DE;&#x7C7B;&#x578B; &#xFF08;Optional Tuple Return Types&#xFF09;</a>.</li>
          <li>&#x66F4;&#x65B0;&#x7AE0;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-XID_453">&#x7C7B;&#x578B;&#x6807;&#x6CE8;&#xFF08;Type Annotations&#xFF09;</a> &#xFF1A;&#x591A;&#x4E2A;&#x76F8;&#x5173;&#x53D8;&#x91CF;&#x53EF;&#x4EE5;&#x7528;&#x201C;&#x7C7B;&#x578B;&#x6807;&#x6CE8;&#x201D;&#xFF08;type
            annotaion&#xFF09;&#x5728;&#x540C;&#x4E00;&#x884C;&#x4E2D;&#x58F0;&#x660E;&#x4E3A;&#x540C;&#x4E00;&#x7C7B;&#x578B;&#x3002;</li>
          <li> <code>@optional</code>, <code>@lazy</code>, <code>@final</code>, <code>@required</code> &#x7B49;&#x5173;&#x952E;&#x5B57;&#x88AB;&#x66F4;&#x65B0;&#x4E3A; <code>optional</code>, <code>lazy</code>, <code>final</code>, <code>required</code> 
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-XID_705">&#x53C2;&#x89C1;&#x58F0;&#x660E;&#x4FEE;&#x9970;&#x7B26;&#xFF08;Declaration
              Modifiers&#xFF09;</a>.</li>
          <li>&#x66F4;&#x65B0;&#x6574;&#x672C;&#x4E66; &#x2014;&#x2014; &#x5F15;&#x7528; <code>..&lt;</code> &#x4F5C;&#x4E3A;
            <a
            href="https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter1/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-XID_128">&#x533A;&#x95F4;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Half-Open Range Operator&#xFF09;</a>(&#x53D6;&#x4EE3;&#x539F;&#x5148;&#x7684;<code>..</code> ).</li>
          <li>&#x66F4;&#x65B0;&#x4E86;&#x5C0F;&#x8282; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_185">&#x8BFB;&#x53D6;&#x548C;&#x4FEE;&#x6539;&#x5B57;&#x5178;&#xFF08;Accessing and Modifying a Dictionary&#xFF09;</a>&#xFF1A; <code>Dictionary</code> &#x73B0;&#x5728;&#x65E9;&#x5462;&#x66F4;&#x52A0;&#x4E86;&#x4E00;&#x4E2A;
            Boolean &#x578B;&#x7684;&#x5C5E;&#x6027;&#xFF1A; <code>isEmpty</code>
          </li>
          <li>&#x89E3;&#x91CA;&#x4E86;&#x54EA;&#x4E9B;&#x5B57;&#x7B26;&#xFF08;&#x96C6;&#xFF09;&#x53EF;&#x88AB;&#x7528;&#x6765;&#x5B9A;&#x4E49;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_85">&#x81EA;&#x5B9A;&#x4E49;&#x64CD;&#x4F5C;&#x7B26; &#xFF08;Custom Operators&#xFF09;</a>
          </li>
          <li> <code>nil</code> &#x548C;&#x5E03;&#x5C14;&#x8FD0;&#x7B97;&#x4E2D;&#x7684; <code>true</code> &#x548C; <code>false</code> &#x73B0;&#x5728;&#x88AB;&#x5B9A;&#x4E49;&#x4E3A;&#x5B57;&#x9762;&#x91CF;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_886">Literals</a>.</li>
          <li>Swift &#x4E2D;&#x7684;&#x6570;&#x7EC4; &#xFF08;<code>Array</code>&#xFF09;
            &#x7C7B;&#x578B;&#x4ECE;&#x73B0;&#x5728;&#x8D77;&#x5177;&#x5907;&#x4E86;&#x5B8C;&#x6574;&#x7684;&#x503C;&#x8BED;&#x4E49;&#x3002;&#x5177;&#x4F53;&#x4FE1;&#x606F;&#x88AB;&#x66F4;&#x65B0;&#x5230;
            <a
            href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_170">&#x96C6;&#x5408;&#x7684;&#x53EF;&#x53D8;&#x6027;&#xFF08;Mutability of
              Collections&#xFF09;</a>&#x548C; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_172">&#x6570;&#x7EC4;&#xFF08;Arrays&#xFF09;</a> &#x4E24;&#x5C0F;&#x8282;&#xFF0C;&#x4EE5;&#x53CD;&#x6620;&#x8FD9;&#x4E2A;&#x65B0;&#x7684;&#x53D8;&#x5316;&#x3002;
              &#x6B64;&#x5916;&#xFF0C;&#x8FD8;&#x89E3;&#x91CA;&#x4E86;&#x5982;&#x4F55;
              <a
              href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/ClassesAndStructures.html#//apple_ref/doc/uid/TP40014097-CH13-XID_150">&#x7ED9; Strings, Arrays &#x548C; Dictionaries &#x8FDB;&#x884C;&#x8D4B;&#x503C;&#x548C;&#x62F7;&#x8D1D;
                &#xFF08;Assignment and Copy Behavior for Strings, Arrays, and Dictionaries&#xFF09;</a>.</li>
          <li> <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_173">&#x6570;&#x7EC4;&#x7C7B;&#x578B;&#x901F;&#x8BB0;&#x8BED;&#x6CD5;&#xFF08;Array Type Shorthand Syntax&#xFF09;</a> &#x4ECE; <code>SomeType[]</code>.&#x66F4;&#x65B0;&#x4E3A;<code>[SomeType]</code>
          </li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x5C0F;&#x8282;&#xFF1A;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_182">&#x5B57;&#x5178;&#x7C7B;&#x578B;&#x7684;&#x901F;&#x8BB0;&#x8BED;&#x6CD5;&#xFF08;Dictionary Type Shorthand Syntax)</a>.&#xFF1A; <code>[KeyType: ValueType]</code>.</li>
          <li>&#x52A0;&#x5165;&#x65B0;&#x7684;&#x5C0F;&#x8282;&#xFF1A;<a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/CollectionTypes.html#//apple_ref/doc/uid/TP40014097-CH8-XID_189">&#x5B57;&#x5178;&#x952E;&#x7C7B;&#x578B;&#x7684;&#x54C8;&#x5E0C;&#x503C;&#xFF08;Hash Values for Dictionary Key Types)</a>.</li>
          <li>&#x4F8B;&#x5B50; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-XID_154">&#x95ED;&#x5305;&#x8868;&#x8FBE;&#x5F0F;&#xFF08;Closure Expressions&#xFF09;</a> &#x4E2D;&#x4F7F;&#x7528;&#x65B0;&#x7684;&#x5168;&#x5C40;&#x51FD;&#x6570; <code>sorted</code> &#x53D6;&#x4EE3;&#x539F;&#x5148;&#x7684;&#x5168;&#x5C40;&#x51FD;&#x6570; <code>sort</code> &#x53BB;&#x5C55;&#x793A;&#x5982;&#x4F55;&#x8FD4;&#x56DE;&#x4E00;&#x4E2A;&#x5168;&#x65B0;&#x7684;&#x6570;&#x7EC4;&#x3002;</li>
          <li>&#x66F4;&#x65B0;&#x5173;&#x4E8E; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-XID_320">&#x7ED3;&#x6784;&#x4F53;&#x9010;&#x4E00;&#x6210;&#x5458;&#x6784;&#x9020;&#x5668; &#xFF08;Memberwise Initializers for Structure Types&#xFF09;</a> &#x7684;&#x63CF;&#x8FF0;&#xFF1A;&#x5373;&#x4F7F;&#x7ED3;&#x6784;&#x4F53;&#x7684;&#x6210;&#x5458;<b>&#x6CA1;&#x6709;&#x9ED8;&#x8BA4;&#x503C;</b>&#xFF0C;&#x9010;&#x4E00;&#x6210;&#x5458;&#x6784;&#x9020;&#x5668;&#x4E5F;&#x53EF;&#x4EE5;&#x81EA;&#x52A8;&#x83B7;&#x5F97;&#x3002;</li>
          <li> <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-XID_128">&#x533A;&#x95F4;&#x8FD0;&#x7B97;&#x7B26;&#xFF08;Half-Open Range Operator&#xFF09;</a>&#x7531;<code>..</code>&#x66F4;&#x65B0;&#x5230;<code>..&lt;</code>
          </li>
          <li>&#x6DFB;&#x52A0;&#x4E00;&#x4E2A;&#x4F8B;&#x5B50; <a href="https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-XID_285">&#x6269;&#x5C55;&#x4E00;&#x4E2A;&#x6CDB;&#x578B;&#xFF08;Extending a Generic Type&#xFF09;</a>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>