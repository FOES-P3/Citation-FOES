Citation-FOES
=============
<?xml version="1.0" encoding="utf-8"?>
<style class="in-text" version="1.0" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="3" et-al-use-first="1" et-al-subsequent-min="3" et-al-subsequent-use-first="1" initialize-with=". " name-as-sort-order="all" demote-non-dropping-particle="never" xmlns="http://purl.org/net/xbiblio/csl">
  <info>
    <title>FOES</title>
    <title-short>Foes</title-short>
    <id>http://www.zotero.org/styles/Foes</id>
    <link href="http://www.zotero.org/styles/foes" rel="self"/>
    <link href="http://owl.english.purdue.edu/owl/resource/560/01/" rel="documentation"/>
    <author>
      <name>Johannes Besch</name>
      <email>j.besch@gmx.net</email>
    </author>
    <category citation-format="author-date"/>
    <updated>2013-12-10T18:06:47+00:00</updated>
    <link/>
  </info>
  <locale xml:lang="en">
    <terms>
      <term name="editortranslator" form="short">
        <single>ed. &amp; trans.</single>
        <multiple>eds. &amp; trans.</multiple>
      </term>
      <term name="translator" form="short">
        <single>trans.</single>
        <multiple>trans.</multiple>
      </term>
    </terms>
  </locale>
  <macro name="author">
    <names variable="author">
      <name delimiter-precedes-last="always" et-al-min="50" et-al-use-first="50" et-al-subsequent-min="50" et-al-subsequent-use-first="50" initialize-with=". " name-as-sort-order="all"/>
      <label form="short" text-case="capitalize-first" prefix=" (" suffix=")"/>
     <choose>
       <if variable="editor">
      <substitute>
      
        <names variable="editor"/>
        <name delimiter="/" delimiter-precedes-last="always" et-al-min="50" et-al-use-first="50" et-al-subsequent-min="50" et-al-subsequent-use-first="50" initialize-with=". " name-as-sort-order="all"/>

      </substitute>
       </if>
      </choose>
    </names>
    </macro>
  <macro name="author-short">
    <names variable="author" delimiter=", ">
      <name form="short" delimiter="/" et-al-min="3" et-al-use-first="1" et-al-subsequent-min="3" et-al-subsequent-use-first="1" initialize-with=". "/>
    </names>
  </macro>
  <macro name="issued">
    <choose>
      <if variable="issued" disambiguate="true">
        <date delimiter="" variable="issued" prefix=" (" suffix=")">
          <date-part name="year"/>
        </date>
      </if>
    </choose>
  </macro>
  <macro name="issued-year">
    <choose>
      <date variable="issued">
        <date-part name="year"/>
      </date>
    </choose>
  </macro>
  <macro name="title">
    <choose>
      <text variable="title" font-style="normal" suffix=". "/>
    </choose>
  </macro>
  <macro name="locators">
    <choose>
      <if type="article-journal">
        <text variable="container-title" font-style="normal" prefix="In: " suffix="."/>
        <group prefix=" ">
          <text variable="volume" font-style="normal" prefix="Jg. " suffix=", "/>
          <text variable="issue" prefix="Nr. " suffix="."/>
        </group>
        <group>
          <text variable="page" prefix=" S. " suffix="."/>
        </group>
      </if>
      <if type="chapter">
        <names variable="editor" prefix="In: " suffix=" (Hg.): " name-as-sort-order="all"/>
        <name variable="editor" delimiter="/"/>
        <text variable="container-title" suffix=". "/>
      </if>
    </choose>
  </macro>
  <macro name="access">
    <choose>
      <if variable="publisher-place">
        <text variable="publisher-place" suffix="."/>
      </if>
      <if variable="URL">
        <group>
          <text value="Abrufbar unter: " prefix=". "/>
          <text variable="URL" suffix=". "/>
          <text value="Letzter Zugriff am: "/>
          <date variable="accessed">
            <date-part name="day" suffix="."/>
            <date-part name="month" suffix="." form="numeric"/>
            <date-part name="year" suffix="." form="numeric"/>
          </date>
        </group>
      </if>
    </choose>
  </macro>
  <citation et-al-min="6" et-al-use-first="1" et-al-subsequent-min="3" et-al-subsequent-use-first="1" disambiguate-add-givenname="true" disambiguate-add-year-suffix="true" givenname-disambiguation-rule="all-names">
    <sort>
      <key macro="author"/>
      <key macro="issued-sort"/>
    </sort>
    <layout prefix="(" suffix=")" delimiter="; ">
      <group delimiter=" ">
        <text macro="author-short"/>
        <text macro="issued-year"/>
      </group>
    </layout>
  </citation>
  <bibliography initialize-with="" entry-spacing="0" line-spacing="2" hanging-indent="true">
    <sort>
      <key macro="author"/>
      <key macro="issued-sort" sort="ascending"/>
    </sort>
    <layout>
      <group>
        <text macro="author"/>
        <text macro="issued" suffix=":"/>
        <text macro="title" prefix=" "/>
        <text macro="locators"/>
        <text macro="access" prefix="" suffix="."/>
      </group>
    </layout>
  </bibliography>
</style>
