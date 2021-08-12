---
title: translateX()
slug: Web/CSS/transform-function/translateX()
tags:
  - CSS
  - CSS Function
  - CSS Transforms
  - Function
  - Reference
browser-compat: css.types.transform-function.translateX
---
<div>{{CSSRef}}</div>

<p>The <strong><code>translateX()</code></strong> <a href="/en-US/docs/Web/CSS">CSS</a> <a
    href="/en-US/docs/Web/CSS/CSS_Functions">function</a> repositions an element horizontally on the 2D plane. Its
  result is a {{cssxref("&lt;transform-function&gt;")}} data type.</p>

<p><img alt="" src="transform-functions-translatex_2.png"></p>

<div class="note">
  <p><strong>Note:</strong> <code>translateX(tx)</code> is equivalent to
    <code><a href="/en-US/docs/Web/CSS/transform-function/translate()">translate</a>(tx, 0)</code> or
    <code><a href="/en-US/docs/Web/CSS/transform-function/translate3d()">translate3d</a>(tx, 0, 0)</code>.
  </p>
</div>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: css">/* &lt;length-percentage&gt; values */
transform: translateX(200px);
transform: translateX(50%);
</pre>

<h3 id="Values">Values</h3>

<dl>
  <dt><code>&lt;length-percentage&gt;</code></dt>
  <dd>Is a {{cssxref("&lt;length&gt;")}} or {{cssxref("&lt;percentage&gt;")}} representing the abscissa of the
    translating vector. A percentage value refers to the width of the reference box defined by the
    {{cssxref("transform-box")}} property.</dd>
</dl>

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col">Cartesian coordinates on ℝ^2</th>
      <th scope="col">Homogeneous coordinates on ℝℙ^2</th>
      <th scope="col">Cartesian coordinates on ℝ^3</th>
      <th scope="col">Homogeneous coordinates on ℝℙ^3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">
        <p>A translation is not a linear transformation in ℝ^2 and can't be represented using a
          Cartesian-coordinate matrix.</p>
      </td>
      <td><math>
          <mfenced>
            <mtable>
              <mtr>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mi>t</mi>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
              </mtr>
            </mtable>
          </mfenced>
        </math></td>
      <td rowspan="2"><math>
          <mfenced>
            <mtable>
              <mtr>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mi>t</mi>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
              </mtr>
            </mtable>
          </mfenced>
        </math></td>
      <td rowspan="2"><math>
          <mfenced>
            <mtable>
              <mtr>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mi>t</mi>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
              </mtr>
              <mtr>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>0</mn>
                </mtd>
                <mtd>
                  <mn>1</mn>
                </mtd>
              </mtr>
            </mtable>
          </mfenced>
        </math></td>
    </tr>
    <tr>
      <td><code>[1 0 0 1 t 0]</code></td>
    </tr>
  </tbody>
</table>

<h3 id="Formal_syntax">Formal syntax</h3>

<pre class="brush: css">translateX({{cssxref("&lt;length-percentage&gt;")}})
</pre>

<h2 id="Examples">Examples</h2>

<h3 id="HTML">HTML</h3>

<pre class="brush: html">&lt;div&gt;Static&lt;/div&gt;
&lt;div class="moved"&gt;Moved&lt;/div&gt;
&lt;div&gt;Static&lt;/div&gt;</pre>

<h3 id="CSS">CSS</h3>

<pre class="brush: css">div {
  width: 60px;
  height: 60px;
  background-color: skyblue;
}

.moved {
  transform: translateX(10px); /* Equal to translate(10px) */
  background-color: pink;
}
</pre>

<h3 id="Result">Result</h3>

<p>{{EmbedLiveSample("Examples", 250, 250)}}</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
  <li><code><a href="/en-US/docs/Web/CSS/transform-function/translate">translate()</a></code></li>
  <li><code><a href="/en-US/docs/Web/CSS/transform-function/translateY">translateY()</a></code></li>
  <li>{{cssxref("transform")}}</li>
  <li>{{cssxref("&lt;transform-function&gt;")}}</li>
</ul>