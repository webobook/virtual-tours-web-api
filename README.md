Welcome to the EvoVR documentation - API for integrating virtual tours into web applications!

# Integrate virtual tours into your site or portal in a few easy steps.

## Introduction

Looking for a quick and easy way to integrate virtual tours and immersive virtual reality into your website or blog? Use the EvoVR API provided by WeboBook.

EevoVr is a tool for creating and visualizing virtual tours with immersive virtual reality, it can be integrated into any site or portal with multiple accounts via API.

## API integration

EvoVr consists of two parts, EvoVR Editor and EvoVR Player. The integration of EvoVR Editor and EvoVR Player is done separately.

EvoVR Editor is the tool used to create and edit virtual tours. Integrates in the administrative part of the site, where ads or posts are created or edited.

EvoVR Player is the player that visualizes virtual tours in front of the end user. It must be integrated in the public part of the site, where ads or posts are displayed to end users.

The architecture of EvoVR is built so that it can be integrated into any type of site, both in blogs or corporate sites and in large portals with multiple separate accounts.

## EvoVR Editor integration

There are three steps to add an EvoVR Editor.

Editor integration should be in the admin panel of your site where your ads or posts are created and edited.

There are three steps to add an EvoVR Editor.

Editor integration should be in the admin panel of your site where your ads or posts are created and edited.

* Step 1: Add the CSS link.
* Step 2: Add the JS links, authenticate the application and specify the language.
* Step 3: Add an HTML tag and make the necessary settings.

### Step 1: Add the CSS link
Copy and paste the <code class="highlighter-rouge">&lt;link&gt;</code> styles into the <code class="highlighter-rouge">&lt;head&gt;</code> section of your page.

<figure class="highlight"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;link</span> <span class="na">rel=</span><span class="s">"stylesheet"</span> <span class="na">href=</span><span class="s">"https://webobook.com/css/evovr.css"</span><span class="nt">&gt;</span></code></pre></figure>

### Step 2: Add the JS links, authenticate the application and specify the language

<p><strong>Step 2-1: </strong> Place the following <code class="highlighter-rouge">&lt;script&gt;</code> at the bottom of your pages, just before the closing <code class="highlighter-rouge">&lt;/body&gt;</code> tag, to enable them. <br>
</p>

<p>Important!</p>
<p>If you have integrated <strong>jQuery</strong> on your site, use the code from the <strong>"Without jQuery"</strong>.<br>
If you do not have integrated <strong>jQuery</strong> on your site, use the code from the <strong>"With jQuery"</strong>.<br>
In order for EvoVR to work, you need the jQuery library, but if you are already loading it on your site, you need to put the javascript link, which is without the jQuery library. <br>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/as:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span> - Without jQuery <br>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/af:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span> - With jQuery
</p>

Without jQuery
<figure class="highlight" style="margin: 0px;"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/as:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/api/asset/u:VIEW_API_KEY,EDIT_API_KEY,YOUR_LANGULAGE"</span><span class="nt">&gt;&lt;/script&gt;</span></code></pre></figure>

or with With jQuery
<figure class="highlight" style="margin: 0px;"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/af:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/api/asset/u:VIEW_API_KEY,EDIT_API_KEY,YOUR_LANGULAGE"</span><span class="nt">&gt;&lt;/script&gt;</span></code></pre></figure>

<p><strong>Step 2-2: </strong>Follow these steps to get API keys and verify the application:</p>

<ol>
  <li>Go to the <a href="http://webobook.com/register-domain" target="_blank"><strong>API Keys</strong></a> tab in <strong>Account settings</strong>.</li>
  <li>In the <strong>Domain name</strong> field, enter the name of the domain for which you want to generate API keys.</li>
  <li>Click <strong>Add</strong> to generate API keys for the specified domain.</li>
  <li>From the list below, copy the first API key from the <strong>View token</strong> column and paste it in place of <code><span class="s">"VIEW_API_KEY"</span></code>  in the two JS links you placed on your site.</li>
  <li>From the list, copy the second API key from the <strong>Edit token</strong> column and paste it in place of <code><span class="s">"EDIT_API_KEY"</span></code> in the second JS connection.</li>
</ol>

<p><strong>Step 2-3: </strong>Set the application language.</p>

<p>
  To set the application language, replace <code><span class="s">"YOUR_LANGULAGE"</span></code> with the corresponding value from the Language code column in the table below.
</p>

<table>
                <thead>
                  <tr>
                    <th style="width:25%">Language code</th>
                    <th style="width:75%">The language</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">en</span></code></code></td>
                    <td>English</td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">bg</span></code></code></td>
                    <td>Bulgarian</td>
                  </tr>
                </tbody>
              </table>

### Step 3: Add an HTML tag and make the necessary settings

<p><strong>Step 3-1: </strong>Place the <code class="highlighter-rouge">&lt;html&gt;</code> tag on your page where you want the editor button to appear.</p>

<figure class="highlight"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;div </span><span class="na">class=</span><span class="s">"evovr-tour-editor"</span> <span class="na">postid=</span><span class="s">"POST_ID"</span> <span class="na">showGadget=</span><span class="s">"true"</span> <span class="na">buttonColor=</span><span class="s">"gray"</span> <span class="na">showIcon=</span><span class="s">"true"</span> <span class="na">editText=</span><span class="s">"Edit Virual Tour"</span> <span class="na">createText=</span><span class="s">"Create Virtual Tour"</span><span class="nt">&gt;&lt;/div&gt;</span>
</code></pre></figure>

<p><strong>Step 3-2: </strong> Enter a value for <code><span class="na">postid</span></code> and make the desired settings.</p>
<p>Submitting a value to <code><span class="na">postid</span></code> is required, <code><span class="na">postid</span></code> initializes the virtual tour.</p>

<p> For <code><span class="na">postid</span></code> you can set a variable with the ID number of your ad or post. Put the variable in place of the <span class="s">"POST_ID"</span>.</p>

<p>Table with additional settings:</p>

<table>
                <thead>
                  <tr>
                    <th>Settings</th>
                    <th>Description</th>
                  </tr>
                </thead>
                <tbody>
                <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">class=</span><span class="s">"evovr-tour-editor"</span></code></code></td>
                    <td>
					Class of the element that calls EvoVR Editor. EvoVR Editor can be called from any html element with class "evovr-tour-editor".
<br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">class=</span><span class="s">"evovr-tour-editor"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><a href="#postid"> <code><span class="na">postid</span></code></a></code></td>
                    <td>
					Your ad or post ID. Replace the <code><span class="s">POST_ID</span></code> with the ID of your ad or post.
<br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">postid=</span><span class="s">"1000"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">showGadget</span></code></code></td>
                    <td>
					Widget that includes a button and icon for EvoVR - Editor. <code><span class="na">showGadget</span></code> can have values <code><span class="s">false</span></code> (disable the widget) or  <code><span class="s">true</span></code> (enable the widget)<br>
                    Type: <code>Boolean</code><br>
                    Example: <code>false, true</code><br>
                    Example: <code><span class="na">showGadget=</span><span class="s">"true"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">buttonColor</span></code></code></td>
                    <td>
					If the widget is enabled (<span class="na">showGadget=</span><span class="s">"true"</span>),  you can adjust the color of the button. Possible values for <code><span class="na">buttonColor</span></code> are <code><span class="s">gray, blue, gray, green, red</span></code>.<br>
                    Type: <code>string</code><br>
                    Example: <code>blue, gray, green, red</code><br>
                    Default: <code>gray</code><br>
                    Example: <code><span class="na">buttonColor=</span><span class="s">"blue"</span></code>
                    </td>
                  </tr>
                   <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">showIcon</span></code></code></td>
                    <td>
					If the widget is enabled (<span class="na">showGadget=</span><span class="s">"true"</span>), you can set whether to display an icon in the widget. Possible values are <code><span class="s">false</span></code> (does not show an icon) or <code><span class="s">true</span></code> (shows an icon).<br>
                    Type: <code>Boolean</code><br>
                    Example: <code>false, true</code><br>
                    Default: <code>true</code><br>
                    Example: <code><span class="na">showIcon=</span><span class="s">"true"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">editText</span></code></code></td>
                    <td>
					If the widget is enabled (<code><span class="na">showGadget=</span><span class="s">"true"</span></code>), you can place custom text on the edit button of the virtual tour in the widget. For example, you can change <code><span class="na">editText=</span><span class="s">"Edit Virual Tour"</span></code> to <code><span class="na">editText=</span><span class="s">"Edit My Virual Tour"</span></code>. <br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">editText=</span><span class="s">"Edit My Virtual Tour"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">createText</span></code></code></td>
                    <td>
					If the widget is enabled (<code><span class="na">showGadget=</span><span class="s">"true"</span></code>), you can place custom text on the button to create the virtual tour. For example, you can change <code><span class="na">createText=</span><span class="s">"Create Virtual Tour"</span></code> to <code><span class="na">createText=</span><span class="s">"Create My Virtual Tour"</span></code>. <br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">createText=</span><span class="s">"Create New Virtual Tour"</span></code>
                    </td>
                  </tr>
                </tbody>
              </table>

### Try it yourself

<p>Copy the code below and create a test page on your site to experiment.</p>
<p>Be sure to generate <a target="_blank" href="http://webobook.com/register-domain"><strong>API keys</strong></a> for your domain and place the corresponding keys in place of <code><span class="s">"VIEW_API_KEY"</span></code> and <code><span class="s">"EDIT_API_KEY"</span></code> in the JS connection.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Editor:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">div</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-editor"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">buttonColor</span><span style="color: #666666">=</span><span style="color: #BA2121">"gray"</span> <span style="color: #7D9029">showGadget</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">showIcon</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">editText</span><span style="color: #666666">=</span><span style="color: #BA2121">"Create a tour"</span> <span style="color: #7D9029">createText</span><span style="color: #666666">=</span><span style="color: #BA2121">"Edit tour"</span> &gt;Open&lt;/<span style="color: #2f6f9f;">div</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/api/asset/u:VIEW_API_KEY,EDIT_API_KEY,en"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

## EvoVR Player integration

<p>There are three steps to integrating the EvoVR Player. The integration of the player should be in the public part of your site where your ads or posts are displayed to the end user.</p>

<ol>
  <li>Step 1: Add the CSS link.</li>
  <li>Step 2: Add the JS links, authenticate the application and specify the language.</li>
  <li>Step 3: Add an HTML tag and make the necessary settings.</li>
</ol>

### Step 1: Add the CSS link
<p>Copy and paste the <code class="highlighter-rouge">&lt;link&gt;</code> styles into the <code class="highlighter-rouge">&lt;head&gt;</code> section of your page.</p>
<figure class="highlight"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;link</span> <span class="na">rel=</span><span class="s">"stylesheet"</span> <span class="na">href=</span><span class="s">"https://webobook.com/css/evovr-preview.css"</span><span class="nt">&gt;</span></code></pre></figure>

### Step 2: Add the JS links, authenticate the application and set the language

<p><strong>Step 2-1: </strong> Paste <code class="highlighter-rouge">&lt;script&gt;</code> at the bottom of your pages, just before the closing <code class="highlighter-rouge">&lt;/body&gt;</code> tag, to enable them.<br>
	</p>
<p style="color:red">Important!</p>
<p>If you have integrated <strong>jQuery</strong> on your site, use the code from the <strong>"Without jQuery"</strong> tab.<br>
If you do not have integrated <strong>jQuery</strong> on your site, use the code from the <strong>"With jQuery"</strong> tab.<br>
In order for EvoVR to work, you need the jQuery library, but if you are already loading it on your site, you need to put the javascript link, which is without the jQuery library. <br>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/as:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span> - Without jQuery <br>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/af:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span> - With jQuery
</p>

Without jQuery
<figure class="highlight" style="margin: 0px;"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/as:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/c:VIEW_API_KEY,YOUR_LANGULAGE"</span><span class="nt">&gt;&lt;/script&gt;</span></code></pre></figure>

or with With jQuery
<figure class="highlight" style="margin: 0px;"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/af:VIEW_API_KEY"</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;script</span> <span class="na">src=</span><span class="s">"https://webobook.com/asset/c:VIEW_API_KEY,YOUR_LANGULAGE"</span><span class="nt">&gt;&lt;/script&gt;</span></code></pre></figure>

<p><strong>Step 2-2:</strong> Follow these steps to get an API key if you dont already have and verify EvoVR Player:</p>

<ol>
  <li>Go to the <a target="_blank" href="http://webobook.com/register-domain"><strong>API Keys</strong></a> tab in <strong>Account settings</strong>.</li>
  <li>(If you have already generated an API key for your site, skip this step.) If you have not yet generated an API key for your site, in the <strong>Domain name</strong> field, enter the domain name for which you want to generate an API key..</li>
  <li>(If you have already generated an API key for your site, skip this step.) Click <strong>Add</strong> to generate API keys for the specified domain.</li>
  <li>From the list below, copy the first API key from the <strong>View token</strong> column and paste it in place of <code><span class="s">"VIEW_API_KEY"</span></code> in the two JS links you posted on your site.</li>
</ol>

<p><strong>Стъпка 2-3: </strong> Set the language of the application.</p>

<p>
  To set the application language, replace <code><span class="s">"YOUR_LANGULAGE"</span></code> with the corresponding value from the Language code column in the table below.
</p>

<table>
                <thead>
                  <tr>
                    <th style="width:25%">Language code</th>
                    <th style="width:75%">The language</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">en</span></code></code></td>
                    <td>English</td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">bg</span></code></code></td>
                    <td>Bulgarian</td>
                  </tr>
                </tbody>
              </table>

### Step 3: Add an HTML tag and make the necessary settings

<p><strong>Step 3-1: </strong>Put the following <code class="highlighter-rouge">&lt;html&gt;</code> on your page where you want EvoVR Player to appear.</p>

<figure class="highlight"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;div </span><span class="na">class=</span><span class="s">"evovr-tour-loader"</span> <span class="na">postid=</span><span class="s">"POST_ID"</span> <span class="na">showIFrame=</span><span class="s">"true"</span> <span class="na">showGadget=</span><span class="s">"false"</span> <span class="na">showIcon=</span><span class="s">"false"</span> <span class="na">buttonColor=</span><span class="s">""</span> <span class="na">text=</span><span class="s">""</span> <span class="na">style=</span><span class="s">"width:250px; text-align:center;"</span><span class="nt">&gt;&lt;/div&gt;</span>
</code></pre></figure>

<p>This embedding method will load the virtual tour in Iframe directly. If you dont want the virtual tour to load directly, see the <a href="#SettingsPlayer">advanced settings</a> table or other embedding examples in the <a href="#examples">examples section</a>.</p>

<p><strong>Step 3-2: </strong> Set a value for  <code><span class="na">postid</span></code> and make the desired settings.
	</p>
<p>Submitting a value to <code><span class="na">postid</span></code> is required, <code><span class="na">postid</span></code> postid initializes the virtual tour.</p>
<p> For <code><span class="na">postid</span></code> you can set a variable with the ID number of your ad or post. Put the variable in place of the <span class="s">"POST_ID"</span>.</p>

### Additional settings for EvoVR Player:

<p>Check if the virtual tour is published.</p>

<figure class="highlight" style="margin: 0px;"><pre><code class="language-html" data-lang="html"><span class="s">https://webobook.com/public/ct:VIEW_API_KEY,</span><span class="s">POST_ID</span></code></pre></figure>

<p>
This URL returns the status of the virtual tour in XML format.<br>
If the result is 0 the virtual tour is not published if the result is 1 the virtual tour is published.<br>
1. Insert your <strong>API key</strong> from the <strong>View token</strong> in place of <code><span class="s">"VIEW_API_KEY"</span></code>.<br>
2. Put your ad or <strong>post ID</strong> in place of <code><span class="s">"POST_ID"</span></code>.
</p>

<table>
                <thead>
                  <tr>
                    <th>Settings</th>
                    <th>Description</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">class=</span><span class="s">"evovr-tour-loader"</span></code></code></td>
                    <td>
					Class of the element that calls EvoVR Player. EvoVR Player can be called from any html element with class "evovr-tour-loader".
<br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">class=</span><span class="s">"evovr-tour-loader"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><a href="#postid"> <code><span class="na">postid</span></code></a></code></td>
                    <td>
					Your ad or post ID. Replace the <code><span class="s">POST_ID</span></code> with the ID of your ad or post.
<br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">postid=</span><span class="s">"1000"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><a href="#postid"> <code><span class="na">showIFrame</span></code></a></code></td>
                    <td>
					Loads the virtual tour in the iframe.<br>
                    Type: <code>Boolean</code><br>
                    Example: <code>false, true</code><br>
                    Example: <code><span class="na">showIFrame=</span><span class="s">"true"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">showGadget</span></code></code></td>
                    <td>
					Widget that includes a button and icon for EvoVR - Player. <code><span class="na">showGadget</span></code> can have values of <code><span class="s">false</span></code> (disable the widget) or <code><span class="s">true</span></code> (enable the widget).<br> When the widget is activated, the virtual tour opens in a modal window after clicking on it. <br>
Dependencies: <span class="na">showIFrame</span> must be <code><span class="s">false</span></code>, for the widget to activate.<br>
                    Type: <code>Boolean</code><br>
                    Example: <code>false, true</code><br>
                    Default: <code>false</code><br>
                    Example: <code><span class="na">showGadget=</span><span class="s">"true"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">buttonColor</span></code></code></td>
                    <td>
					If the widget is enabled (<span class="na">showGadget=</span><span class="s">"true"</span>) you can adjust the color of the button. Possible values for <code><span class="na">buttonColor</span></code> are <code><span class="s">gray, blue, gray, green, red</span></code>.<br>
                    Type: <code>string</code><br>
                    Example: <code>blue, gray, green, red</code><br>
                    Default: <code>gray</code><br>
                    Example: <code><span class="na">buttonColor=</span><span class="s">"blue"</span></code>
                    </td>
                  </tr>
                   <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">showIcon</span></code></code></td>
                    <td>
					If the widget is enabled (<span class="na">showGadget=</span><span class="s">"true"</span>), you can set whether to display an icon in the widget. Possible values are <code><span class="s">false</span></code> (does not show an icon) or <code><span class="s">true</span></code> (shows an icon).<br>
                    Type: <code>Boolean</code><br>
                    Example: <code>false, true</code><br>
                    Default: <code>true</code><br>
                    Example: <code><span class="na">showIcon=</span><span class="s">"true"</span></code>
                    </td>
                  </tr>
                  <tr>
                    <td><code class="highlighter-rouge"><code><span class="na">text</span></code></code></td>
                    <td>
					If the widget is enabled (<code><span class="na">showGadget=</span><span class="s">"true"</span></code>), you can place custom text on the button in the widget to view the virtual tour.<br>
                    Type: <code>string</code><br>
                    Example: <code><span class="na">text=</span><span class="s">"View the virtual tour"</span></code>
                    </td>
                  </tr>
                </tbody>
              </table>

### Try it yourself

<p>Copy the code below and create a test page on your site to experiment.</p>

<p>Remember to generate <a target="_blank" href="http://webobook.com/register-domain"><strong>API keys</strong></a> (if you havent already) for your domain and place the appropriate key in place of <code><span class="s">"VIEW_API_KEY"</span></code> in the JS connection.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Player:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr-preview.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">div</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-loader"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showIFrame</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">style</span><span style="color: #666666">=</span><span style="color: #BA2121">"width:100%; height:100%"</span>&gt;&lt;/<span style="color: #2f6f9f;">div</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/c:VIEW_API_KEY,bg"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

## Integration in portals with multi-user access.

<p>The EvoVR API can be integrated into multi-user applications. To separate individual users you need to submit the <strong>user id </strong> in place of <code><span class="s">"EDIT_API_KEY"</span></code>.<br>
It is recommended to use a hash function such as <code>hash("sha256", "EDIT_API_KEY");</code>.
The minimum characters to be sent for  <code><span class="s">"EDIT_API_KEY"</span></code>, are 16.<br>
The EvoVR API will prompt your individual users to create a WeboBook account and will connect each individual user to your client in the API.<br>
In this way, each individual user will be able to independently manage their virtual tours.</p>

## Examples

<p>You can experiment with the examples below.<br>
Be sure to generate API keys (if you havent already) for your domain and insert the appropriate key.</p>

### Example of integrating EvoVR Editor without using the widget.

<p>You can call EvoVR Editor from any html element with class <code><span class="s">"evovr-tour-editor"</span></code> and set <code><span class="na">showGadget=</span><span class="s">"false"</span></code>.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Editor:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">button</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-editor"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showGadget</span><span style="color: #666666">=</span><span style="color: #BA2121">"false"</span> &gt;Open&lt;/<span style="color: #2f6f9f;">button</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/api/asset/u:VIEW_API_KEY,EDIT_API_KEY,en"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

### Example of integrating EvoVR Editor using the widget.

<p>You can use the widget, which includes an icon and a button below it, to open the EvoVR Editor.<br>
The widget can be customized, display icon and button or just a button. You can change the color of the button from the preset ones.<br>
You can see the widget setup options in the EvoVR Editor settings table.<br>
The example below will visualize the widget with all possible attributes.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Editor:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">div</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-editor"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showGadget</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">buttonColor</span><span style="color: #666666">=</span><span style="color: #BA2121">"gray"</span> <span style="color: #7D9029">showIcon</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">editText</span><span style="color: #666666">=</span><span style="color: #BA2121">"Edit tour"</span> <span style="color: #7D9029">createText</span><span style="color: #666666">=</span><span style="color: #BA2121">"Create a tour"</span> &gt;Open&lt;/<span style="color: #2f6f9f;">div</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/api/asset/u:VIEW_API_KEY,EDIT_API_KEY,en"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

### Example of integrating EvoVR Player with direct loading of the virtual tour in Iframe.

<p>If you want to load a virtual tour along with loading the page, you must set the <code><span class="na">showIFrame=</span><span class="s">"true"</span></code> attribute. This will load the virtual tour in Iframe while your page loads.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Player:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr-preview.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">div</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-loader"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showIFrame</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">style</span><span style="color: #666666">=</span><span style="color: #BA2121">"width:100%; height:100%"</span>&gt;&lt;/<span style="color: #2f6f9f;">div</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/c:VIEW_API_KEY,bg"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

### Example of integrating EvoVR Player by loading the virtual tour in a modal window.

<p>If you want to load the virtual tour after clicking a button in a full-screen modal window, you can use a custom button or the built-in widget.</p>

<p>For a custom button you need to set the evovr-tour-loader class to the desired html element and set the attributes <code><span class="na">showIFrame=</span><span class="s">"false"</span></code> and <code><span class="na">showGadget=</span><span class="s">"false"</span></code>.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Player:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr-preview.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">button</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-loader"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showIFrame</span><span style="color: #666666">=</span><span style="color: #BA2121">"false"</span> <span style="color: #7D9029">showGadget</span><span style="color: #666666">=</span><span style="color: #BA2121">"false"</span>&gt;&lt;/<span style="color: #2f6f9f;">button</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/c:VIEW_API_KEY,bg"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>

<p>To use the built-in widget, which includes an icon and a button below it, you must set <code><span class="na">showIFrame=</span><span class="s">"false"</span></code> and <code><span class="na">showGadget=</span><span class="s">"true"</span></code>.
The gadget can be customized, display an icon and a button, or display a button only. You can change the color of the button from the preset ones.
You can see the widget options in the EvoVR editor settings table.</p>

<figure class="highlight" style="background: #f8f8f8"><pre style="line-height: 125%"><span></span><span style="color: #BC7A00">&lt;!doctype html&gt;</span>
&lt;<span style="color: #2f6f9f;">html</span>&gt;
&lt;<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">meta</span> <span style="color: #7D9029">charset</span><span style="color: #666666">=</span><span style="color: #BA2121">"utf-8"</span>&gt;
&lt;<span style="color: #2f6f9f;">title</span>&gt;EvoVR-Player:Test&lt;/<span style="color: #2f6f9f;">title</span>&gt;
&lt;<span style="color: #2f6f9f;">link</span> <span style="color: #7D9029">rel</span><span style="color: #666666">=</span><span style="color: #BA2121">"stylesheet"</span> <span style="color: #7D9029">href</span><span style="color: #666666">=</span><span style="color: #BA2121">"https://webobook.com/css/evovr-preview.css"</span>&gt;
&lt;/<span style="color: #2f6f9f;">head</span>&gt;
&lt;<span style="color: #2f6f9f;">body</span>&gt;
&lt;<span style="color: #2f6f9f;">div</span> <span style="color: #7D9029">class</span><span style="color: #666666">=</span><span style="color: #BA2121">"evovr-tour-loader"</span> <span style="color: #7D9029">postid</span><span style="color: #666666">=</span><span style="color: #BA2121">"101"</span> <span style="color: #7D9029">showIFrame</span><span style="color: #666666">=</span><span style="color: #BA2121">"false"</span> <span style="color: #7D9029">showGadget</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">buttonColor</span><span style="color: #666666">=</span><span style="color: #BA2121">"gray"</span> <span style="color: #7D9029">showIcon</span><span style="color: #666666">=</span><span style="color: #BA2121">"true"</span> <span style="color: #7D9029">text</span><span style="color: #666666">=</span><span style="color: #BA2121">"View the virtual tour"</span> <span style="color: #7D9029">style</span><span style="color: #666666">=</span><span style="color: #BA2121">"width:250px; text-align:center;"</span>&gt;&lt;/<span style="color: #2f6f9f;">div</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/af:VIEW_API_KEY"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;<span style="color: #2f6f9f;">script</span> <span style="color: #7D9029">src </span><span style="color: #666666">=</span> <span style="color: #BA2121">"https://webobook.com/asset/c:VIEW_API_KEY,bg"</span>&gt;&lt;/<span style="color: #2f6f9f;">script</span>&gt;
&lt;/<span style="color: #2f6f9f;">body</span>&gt;
&lt;/<span style="color: #2f6f9f;">html</span>&gt;
</pre></figure>
