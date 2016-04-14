# jq_plugin
<p>jqpool.js is a lightweight jQuery plugin that converts poll questions stored in a JSON file into a wizard-like survey interface.</p>

<h2>How to use it:</h2>

<p>1. Create the Html for the survey with next / prev buttons.</p>

<div class="syntaxhighlighter  Brush" id="highlighter_298786" style="font-size: 16px; width: 613.797px; margin: 1em 0px !important; padding: 1px !important; border: 0px !important; outline: 0px !important; vertical-align: baseline !important; float: none !important; position: relative !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; line-height: 1.1em !important; font-family: Consolas, 'Bitstream Vera Sans Mono', 'Courier New', Courier, monospace !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">
<div class="lines" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background: none !important;">
<blockquote>
<div class="line alt1" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">&lt;div class=&quot;question-container&quot;&gt;&lt;/div&gt;<br />
&lt;a id=&quot;backBtn&quot; href=&quot;#&quot; class=&quot;button&quot;&gt;&laquo; Back&lt;/a&gt;<br />
&lt;a id=&quot;nextBtn&quot; href=&quot;#&quot; class=&quot;button&quot;&gt;Continue &raquo;&lt;/a&gt;</div>

<div class="line alt1" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">&nbsp;</div>
</blockquote>
</div>
</div>

<p>2. Prepare your survey questions in the JSON file. The data structure should be like this:</p>

<blockquote>
<pre>
[  
    {  
        "text":"Вопрос 1?",
        "id":"2",
        "break_after":true,
        "required":true,
        "type":"single-select",
        "options":[  
            "Ответ 1",
            "Ответ 2",
            "Ответ 3",
            "Ответ 4"
        ]
    },
    {  
        "text":"Вопрос 2?",
        "id":"3",
        "required":true,
        "type":"single-select",
        "options":[  
            "Ответ 1",
            "Ответ 2",
            "Ответ 3",
            "Ответ 4"
        ]
    },
    {  
        "text":"Вопрос 3?",
        "id":"4",
        "type":"single-select",
        "options":[  
            "Ответ 1",
            "Ответ 2",
            "Ответ 3",
            "Ответ 4"
        ]
    },
    {  
        "text":"Вопрос 4?",
        "id":"5",
        "type":"single-select",
        "options":[  
            "Ответ 1",
            "Ответ 2",
            "Ответ 3"
           
        ]
    },
    {  
        "text":"Вопрос 5?",
        "id":"6",
        "type":"single-select",
        "options":[  
            "Ответ 1",
            "Ответ 2",
            "Ответ 3",
            "Ответ 4"
        ]
   
    }
]</pre>
</blockquote>

<div class="syntaxhighlighter  Brush" id="highlighter_45541" style="font-size: 16px; width: 613.797px; margin: 1em 0px !important; padding: 1px !important; border: 0px !important; outline: 0px !important; vertical-align: baseline !important; float: none !important; position: relative !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; line-height: 1.1em !important; font-family: Consolas, 'Bitstream Vera Sans Mono', 'Courier New', Courier, monospace !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">
<div class="lines" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background: none !important;">&nbsp;</div>
</div>

<p>3. Load jQuery library and the jQuery survey plugin in your web page.</p>

<blockquote>
<pre>
&lt;script src=&quot;//code.jquery.com/jquery-1.11.3.min.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;jqpool.js&quot;&gt;&lt;/script&gt;</pre>
</blockquote>

<div class="syntaxhighlighter  Brush" id="highlighter_52876" style="font-size: 16px; width: 613.797px; margin: 1em 0px !important; padding: 1px !important; border: 0px !important; outline: 0px !important; vertical-align: baseline !important; float: none !important; position: relative !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; line-height: 1.1em !important; font-family: Consolas, 'Bitstream Vera Sans Mono', 'Courier New', Courier, monospace !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">
<div class="lines" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background: none !important;">&nbsp;</div>
</div>

<p>4. Add your own CSS to style the survey.</p>

<blockquote>
<pre>
.question {
  ...
}</pre>
</blockquote>

<div class="syntaxhighlighter  Brush" id="highlighter_413552" style="font-size: 16px; width: 613.797px; margin: 1em 0px !important; padding: 1px !important; border: 0px !important; outline: 0px !important; vertical-align: baseline !important; float: none !important; position: relative !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; line-height: 1.1em !important; font-family: Consolas, 'Bitstream Vera Sans Mono', 'Courier New', Courier, monospace !important; min-height: auto !important; background-image: none !important; background-attachment: initial !important; background-size: initial !important; background-origin: initial !important; background-clip: initial !important; background-position: initial !important; background-repeat: initial !important;">
<div class="lines" style="margin: 0px !important; padding: 0px !important; border: 0px !important; outline: 0px !important; font-size: 1em !important; vertical-align: baseline !important; float: none !important; position: static !important; left: auto !important; top: auto !important; right: auto !important; bottom: auto !important; height: auto !important; width: auto !important; line-height: 1.1em !important; min-height: auto !important; background: none !important;">&nbsp;</div>
</div>
