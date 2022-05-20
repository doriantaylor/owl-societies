## Societies Ontology

<div about="#" typeof="owl:Ontology bibo:Webpage">

  - Author  
    [<span property="foaf:name">Dorian
    Taylor</span>](http://doriantaylor.com/person/dorian-taylor#me)
  - Version  
    0.1
  - Created  
    July 29, 2014
  - Namespace URI  
    <https://vocab.methodandstructure.com/societies#>
  - Preferred Namespace Prefix  
    soco

The Organization Ontology provides a core set of classes and properties
useful for describing the basic structures of corporate entities. The
authors deliberately left out explicit provisions for the myriad
idiosyncrasies we find in organizations all around the world. The
Societies Ontology is an attempt to fill some of that in.

A *society*, charity, association, foundation, or other non-profit
entity tends to be structured according to a common schema. In North
America, at least, a society is controlled by an elected
<span class="dfn">board of directors</span>. Of these directors, there
are the legislated roles of <span class="dfn">president</span>,
<span class="dfn">secretary</span>, and
<span class="dfn">treasurer</span>, and may appoint an
<span class="dfn">executive director</span> to run the organization.

A board of directors is actually a special kind of
<span class="dfn">committee</span>, which itself is a special kind of
<span class="dfn">organizational unit</span>. Societies may also have
members, which themselves may be people, or other organizations. It is
the goal of this vocabulary to provide the necessary extensions to
encode those relationships.

I acknowledge a bias toward the anglosphere, common law, and especially
North America when considering this vocabulary. I am content to take
suggestions to accommodate structures from other jurisdictions.

![](https://vocab.methodandstructure.com/societies-classes)

#### Imports

  - [<span property="rdfs:label" lang="en">Core organization
    ontology</span>](http://www.w3.org/ns/org#)

</div>

<div>

## Classes

<div id="Chapter" about="[soco:Chapter]" typeof="owl:Class">

#### Chapter

A chapter is an organizational unit focused on a geographic region.

  - Subclass of:  
    [org:OrganizationalUnit](http://www.w3.org/ns/org#OrganizationalUnit)

</div>

<div id="Committee" about="[soco:Committee]" typeof="owl:Class">

#### Committee

A committee is a specific type of organizational unit.

  - Subclass of:  
    [org:OrganizationalUnit](http://www.w3.org/ns/org#OrganizationalUnit)

</div>

<div id="Board" about="[soco:Board]" typeof="owl:Class">

#### Board

The board of directors is a specific committee within the organization.

  - Subclass of:  
    [soco:Committee](https://vocab.methodandstructure.com/societies#Committee)
  - Properties:  
    [soco:board-of](https://vocab.methodandstructure.com/societies#board-of)

</div>

</div>

<div>

## Properties

### Related to the Board of Directors

<div id="board-of" about="[soco:board-of]" typeof="owl:InverseFunctionalProperty owl:ObjectProperty">

#### board-of

Indicates a direct relation between a board of directors and its parent
organization.

  - Sub-property of:  
    [org:unitOf](http://www.w3.org/ns/org#unitOf)
  - Inverse of:  
    [soco:has-board](https://vocab.methodandstructure.com/societies#has-board)
  - Domain:  
    [org:Organization](http://www.w3.org/ns/org#Organization)
  - Range:  
    [soco:Board](https://vocab.methodandstructure.com/societies#Board)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="has-board" about="[soco:has-board]" typeof="owl:FunctionalProperty owl:ObjectProperty">

#### has-board

Indicates a direct relation between an organization and its board of
directors.

  - Sub-property of:  
    [org:hasUnit](http://www.w3.org/ns/org#unitOf)
  - Inverse of:  
    [soco:board-of](https://vocab.methodandstructure.com/societies#board-of)
  - Domain:  
    [soco:Board](https://vocab.methodandstructure.com/societies#Board)
  - Range:  
    [org:Organization](http://www.w3.org/ns/org#Organization)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

### Related to Membership

<div id="primary-contact" about="[soco:primary-contact]" typeof="owl:ObjectProperty">

#### primary-contact

Designates the person who is the primary contact of a membership.

> Many membership organizations, e.g. trade or professional
> associations, have companies as members rather than people. In that
> case, the member company would designate a person to deal with the
> details of its membership to the association.

  - Domain:  
    [org:Membership](http://www.w3.org/ns/org#Membership)
  - Range:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="billing-contact" about="[soco:billing-contact]" typeof="owl:ObjectProperty">

#### billing-contact

Designates the person who is in charge of paying the bills associated
with a membership.

> In membership organizations whose members are companies, there is
> often a dedicated bookkeeper, comptroller, or CFO.

  - Domain:  
    [org:Membership](http://www.w3.org/ns/org#Membership)
  - Range:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

### Related to Officers

<div id="president-of" about="[soco:president-of]" typeof="owl:ObjectProperty">

#### president-of

Designates the president of the organization.

  - Sub-property of:  
    [org:headOf](http://www.w3.org/ns/org#headOf)
  - Domain:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)
  - Range:  
    [org:Organization](http://www.w3.org/ns/org#Organization)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="secretary-of" about="[soco:secretary-of]" typeof="owl:ObjectProperty">

#### secretary-of

Designates the secretary of the organization.

  - Sub-property of:  
    [org:memberOf](http://www.w3.org/ns/org#memberOf)
  - Domain:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)
  - Range:  
    [org:Organization](http://www.w3.org/ns/org#Organization)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="treasurer-of" about="[soco:treasurer-of]" typeof="owl:ObjectProperty">

#### treasurer-of

Designates the treasurer of the organization.

  - Sub-property of:  
    [org:memberOf](http://www.w3.org/ns/org#memberOf)
  - Domain:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)
  - Range:  
    [org:Organization](http://www.w3.org/ns/org#Organization)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="executive-director-of" about="[soco:executive-director-of]" typeof="owl:ObjectProperty">

#### executive-director-of

Designates the executive director of the organization.

  - Sub-property of:  
    [org:memberOf](http://www.w3.org/ns/org#memberOf)
  - Domain:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)
  - Range:  
    [org:Organization](http://www.w3.org/ns/org#Organization)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="chair-of" about="[soco:chair-of]" typeof="owl:ObjectProperty">

#### chair-of

Designates the chair of a committee.

  - Sub-property of:  
    [org:memberOf](http://www.w3.org/ns/org#memberOf)
  - Domain:  
    [foaf:Person](http://xmlns.com/foaf/0.1/Person)
  - Range:  
    [soco:Committee](https://vocab.methodandstructure.com/societies#Committee)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

</div>

<div>

## Individuals

This vocabulary contains a number of predefined roles.

<div id="Officers" about="[soco:Officers]" typeof="skos:ConceptScheme">

#### Officers

This is a concept scheme to contain the standard roles of officers.

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="President" about="[soco:President]" typeof="org:Role">

#### President

The president is the elected chief executive of an organization. The
president is the first of three officer roles typically mandated by
legislation.

  - Role property:  
    [soco:president-of](https://vocab.methodandstructure.com/societies#president-of)
  - Concept scheme:  
    [Officers](https://vocab.methodandstructure.com/societies#Officers)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="Secretary" about="[soco:Secretary]" typeof="org:Role">

#### Secretary

The secretary is the elected officer responsible for maintaining the
records of an organization, and is the second of three
typically-mandatory officer roles.

  - Role property:  
    [soco:secretary-of](https://vocab.methodandstructure.com/societies#secretary-of)
  - Concept scheme:  
    [Officers](https://vocab.methodandstructure.com/societies#Officers)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="Treasurer" about="[soco:Treasurer]" typeof="org:Role">

#### Treasurer

The treasurer is the elected officer responsible for the finances of an
organization, and is the third of the three mandatory elected positions.

  - Role property:  
    [soco:treasurer-of](https://vocab.methodandstructure.com/societies#treasurer-of)
  - Concept scheme:  
    [Officers](https://vocab.methodandstructure.com/societies#Officers)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="ExecutiveDirector" about="[soco:ExecutiveDirector]" typeof="org:Role">

#### Executive Director

The executive director is the first appointed position in a society-like
organization, and is responsible for its day-to-day operation.

  - Role property:  
    [soco:executive-director-of](https://vocab.methodandstructure.com/societies#executive-director-of)
  - Concept scheme:  
    [Officers](https://vocab.methodandstructure.com/societies#Officers)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

<div id="Chair" about="[soco:Chair]" typeof="org:Role">

#### Chair

The chair, or chairperson, is in charge of maintaining order in a
committee.

  - Role property:  
    [soco:chair-of](https://vocab.methodandstructure.com/societies#chair-of)
  - Concept scheme:  
    [Officers](https://vocab.methodandstructure.com/societies#Officers)

[Back to Top](https://vocab.methodandstructure.com/societies#)

</div>

</div>
