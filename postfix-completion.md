# Custom postfix-completion

- stringIsBlank
- stringIsNotBlank
- collectionIsEmpty
- collectionIsNotEmpty
- hashmap
- hashset
- arraylist

# Disabled

- assert

# PostfixTemplates

```xml
<application>
  <component name="PostfixTemplates">
    <template id="stringIsBlank@userDefined" key=".stringIsBlank" provider="builtin.java" language-level="7" topmost="false">
      <conditions>
        <condition id="notPrimitive" />
      </conditions>
      <template name="fakeKey" value="org.apache.commons.lang3.StringUtils.isBlank($EXPR$)" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="collectionIsEmpty@userDefined" key=".collectionIsEmpty" provider="builtin.java" language-level="7" topmost="false">
      <conditions />
      <template name="fakeKey" value="cn.hutool.core.collection.CollectionUtil.isEmpty($EXPR$);" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="collectionIsNotEmpty@userDefined" key=".collectionIsNotEmpty" provider="builtin.java" language-level="7" topmost="false">
      <conditions />
      <template name="fakeKey" value="cn.hutool.core.collection.CollectionUtil.isNotEmpty($EXPR$)" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="hashmap@userDefined" key=".hashmap" provider="builtin.java" language-level="8" topmost="true">
      <conditions />
      <template name="fakeKey" value="java.util.Map&lt;$END$, $EXPR$&gt; $END$ = new java.util.HashMap&lt;&gt;();" description="" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="hashset@userDefined" key=".hashset" provider="builtin.java" language-level="8" topmost="false">
      <conditions />
      <template name="fakeKey" value="java.util.Set&lt;$EXPR$&gt; $END$ = new java.util.HashSet&lt;&gt;();" description="" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="arraylist@userDefined" key=".arraylist" provider="builtin.java" language-level="8" topmost="true">
      <conditions />
      <template name="fakeKey" value="java.util.List&lt;$EXPR$&gt; $END$ = new java.util.ArrayList&lt;&gt;();" description="" toReformat="true" toShortenFQNames="true" />
    </template>
    <template id="stringIsNotBlank@userDefined" key=".stringIsNotBlank" provider="builtin.java" language-level="1.3" topmost="false">
      <conditions>
        <condition id="notPrimitive" />
      </conditions>
      <template name="fakeKey" value="org.apache.commons.lang3.StringUtils.isNotBlank($EXPR$)" toReformat="true" toShortenFQNames="true" />
    </template>
  </component>
  <component name="PostfixTemplatesSettings">
    <option name="providerToDisabledTemplates">
      <disabled-templates provider="builtin.java">
        <value>
          <set>
            <option value="assert" />
          </set>
        </value>
      </disabled-templates>
    </option>
  </component>
</application>
```
