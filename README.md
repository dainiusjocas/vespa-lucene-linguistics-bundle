# vespa-lucene-linguistics-bundle

Contains a [Vespa]([url](https://vespa.ai)) [bundle]([url](https://docs.vespa.ai/en/components/bundles.html)) jar with [Lucene Linguistics](https://github.com/vespa-engine/vespa/tree/master/lucene-linguistics) to be used in non-Java Vespa applications.

Instructions:
1. Download a jar from [`Releases`]([url](https://github.com/dainiusjocas/vespa-lucene-linguistics-bundle/releases)) and add it to the application packages `components` directory.

2. Add the [Linguistics]([url](https://docs.vespa.ai/en/linguistics.html)) component specification to the [`services.xml`]([url](https://docs.vespa.ai/en/reference/services.html)) file under the `<container>`:
```xml
<component id="linguistics"
           class="com.yahoo.language.lucene.LuceneLinguistics"
           bundle="lucene-linguistics-bundle">
  <config name="com.yahoo.language.lucene.lucene-analysis">
    <configDir>ext/linguistics</configDir>
  </config>
</component>
```

3. Deploy to Vespa.
   ```shell
   vespa deploy -w 60
   ```

4. Profit.

A demo application package can be found [here](https://github.com/vespa-engine/sample-apps/blob/782080269fe77760b74a2177972f46bf6c340df7/examples/lucene-linguistics/non-java/README.md).
