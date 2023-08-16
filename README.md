# vespa-lucene-linguistics-bundle

Contains a Vespa bundle jar with Lucene Linguistics to be used in non-Java Vespa applications.

Download a jar from `Releases` and add it to the application packages `components` directory.

Add the component specification to the `services.xml` file:
```xml
<component id="linguistics"
           class="com.yahoo.language.lucene.LuceneLinguistics"
           bundle="lucene-linguistics-bundle">
  <config name="com.yahoo.language.lucene.lucene-analysis">
    <configDir>ext/linguistics</configDir>
  </config>
</component>
```

Then deploy to Vespa.

Profit.

TODO: link to the sample app.
