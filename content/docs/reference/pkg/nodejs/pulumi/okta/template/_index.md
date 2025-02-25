---
title: "Module template"
linktitle: "template"
meta_desc: "Explore members of the template module in the @pulumi/okta package."
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->


> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-okta)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-okta` repo](https://github.com/pulumi/pulumi-okta/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-okta` repo](https://github.com/terraform-providers/terraform-provider-okta/issues).





<h3>Resources</h3>
<ul class="api">
    <li><a href="#Email"><span class="symbol resource"></span>Email</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#EmailArgs"><span class="symbol api"></span>EmailArgs</a></li>
    <li><a href="#EmailState"><span class="symbol api"></span>EmailState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Email" data-link-title="Email">
    <a href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L39">
        Resource <strong>Email</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Email</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Creates an Okta Email Template.

This resource allows you to create and configure an Okta Email Template.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as okta from "@pulumi/okta";

const example = new okta.template.Email("example", {
    translations: [
        {
            language: "en",
            subject: "Stuff",
            template: "Hi ${user.firstName},<br/><br/>Blah blah ${resetPasswordLink}",
        },
        {
            language: "es",
            subject: "Cosas",
            template: "Hola ${user.firstName},<br/><br/>Puedo ir al bano ${resetPasswordLink}",
        },
    ],
    type: "email.forgotPassword",
});
```

> This content is derived from https://github.com/articulate/terraform-provider-okta/blob/master/website/docs/r/template_email.html.markdown.

<h4 class="pdoc-member-header" id="Email-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L77"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Email(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#EmailArgs'>EmailArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Email resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Email-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L48">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#EmailState'>EmailState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Email'>Email</a></code></pre>


Get an existing Email resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Email-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L39">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Email-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L59">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></code></pre>


Returns true if the given object is an instance of Email.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Email-defaultLanguage">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L69">property <b>defaultLanguage</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>defaultLanguage: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

The default language, by default is set to `"en"`.

<h4 class="pdoc-member-header" id="Email-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L39">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Email-translations">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L73">property <b>translations</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>translations: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/okta/types/output/#EmailTranslation'>outputs.template.EmailTranslation</a>[]&gt;;</code></pre>

Set of translations for particular template.

<h4 class="pdoc-member-header" id="Email-type">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L77">property <b>type</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>type: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Email template type

<h4 class="pdoc-member-header" id="Email-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L39">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="EmailArgs" data-link-title="EmailArgs">
    <a href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L138">
        interface <strong>EmailArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>EmailArgs</span></code></pre>

The set of arguments for constructing a Email resource.

<h4 class="pdoc-member-header" id="EmailArgs-defaultLanguage">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L142">property <b>defaultLanguage</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>defaultLanguage?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The default language, by default is set to `"en"`.

<h4 class="pdoc-member-header" id="EmailArgs-translations">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L146">property <b>translations</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>translations: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/okta/types/input/#EmailTranslation'>inputs.template.EmailTranslation</a>&gt;[]&gt;;</code></pre>

Set of translations for particular template.

<h4 class="pdoc-member-header" id="EmailArgs-type">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L150">property <b>type</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>type: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Email template type

<h3 class="pdoc-module-header" id="EmailState" data-link-title="EmailState">
    <a href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L120">
        interface <strong>EmailState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>EmailState</span></code></pre>

Input properties used for looking up and filtering Email resources.

<h4 class="pdoc-member-header" id="EmailState-defaultLanguage">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L124">property <b>defaultLanguage</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>defaultLanguage?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The default language, by default is set to `"en"`.

<h4 class="pdoc-member-header" id="EmailState-translations">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L128">property <b>translations</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>translations?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/okta/types/input/#EmailTranslation'>inputs.template.EmailTranslation</a>&gt;[]&gt;;</code></pre>

Set of translations for particular template.

<h4 class="pdoc-member-header" id="EmailState-type">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-okta/blob/63bf98192050cf6907357504e32c0306587565f4/sdk/nodejs/template/email.ts#L132">property <b>type</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>type?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Email template type

