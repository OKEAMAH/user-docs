# Backstage file in Asset Inventory - Use case

After you finish configuring the [Backstage catalog](./#backstage-file-for-scm-integrations), Snyk AppRisk starts enriching your repository assets (the [All Assets](../../../manage-assets/#inventory-overview) tab from the Inventory layout) with the data found in the backstage `catalog .yaml` file.

Use the Backstage catalog to enrich the repository assets and to define the component entity. For this type of situation, a component is defined as a software component, like a service, repository, website, library, and so on.&#x20;

Components have several attributes and most of them are optional:

* `spec.type` (mandatory) - represents the classification of the repository.&#x20;
* `spec.owner` (mandatory) - represents the team owning the repository.
* `spec.lifecycle` - represents the lifecycle state of the component, for example `production`, `experimental`, `deprecated`.
* `spec.system` (optional) - represents a group of components that serve the same purpose. This concept is referred to as “Application”.
* `Metadata.name` (mandatory) - represents the name of the component.
* `Metadata.title` (optional) - represents the name of the component.

The Backstage data is dynamic and may change over time:

* If new commits or updates are made on the `catalog-info.yaml` file, then Snyk AppRisk updates the asset attribute for that specific repository asset.
* If the`catalog-info.yaml` file is removed from the repository, then Snyk AppRisk deletes the asset attribute from that specific repository assets.

## Inventory menu and the Backstage file&#x20;

Depending on the selection you made on the Integration Hub configuration menu, only those selections are displayed in filters from the Inventory menu. For example, if you selected the Category attribute, then it will also be displayed in the filters list.

## Asset Summary Tab and the Backstage file&#x20;

The Asset Summary tab shows the six Backstage attributes that are configured in the Integration Hub only if you choose to integrate with Backstage.

## Asset Attributes Tab and the Backstage file&#x20;

In the Asset Attributes tab only the selected attributes should be added as metadata to the repository asset.

```
{
    name:"spring.goof",
    repositoryURL:"https://github.com/snyk/spring.goof.git",
    context:[
             {
              name: "super-duper-component",
              title: "Super Duper Component",
	      application: "super-duper-app",
	      lifecycle: "production",
	      owner: "super-duper-team",
	      category: "service",
              source: "Backstage"
              }]
}
```

## Policies Filter and the Backstage file&#x20;

In the policy builder you can find only the attributes you have previously selected when configuring the backstage catalog file.&#x20;

The following list describes all possible backstage attributes that you can choose from when you configure the backstage catalog file.&#x20;

* **Application** - represents a group of components that serve the same purpose.&#x20;
* **Owner** - specifies the team owning the repository.
* **Catalog name** - the metadata name.
* **Title** - a name to display for the entity instead of the property. It is an alternative to the metadata name, when the catalog name is too hard to read.
* **Category** - represents the classification of the repository. The Organization can choose any name or text.
* **Lifecycle** - specifies the lifecycle state of the component, for example production, experimental, deprecated.

The following video provides an overview of the Backstage file option from the Integration Hub and a quick explanation of the available attributes:

{% embed url="https://www.youtube.com/watch?v=gfOUSE0UhHA" %}
Liked the video? Checkout the rest of the course on [Snyk Learn](https://learn.snyk.io/catalog/?type=product-training\&topics=AppRisk)!
{% endembed %}