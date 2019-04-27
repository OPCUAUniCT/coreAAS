# **Version 0.2.1**

## New ReferenceType
- Created a new Non Hierarchical ReferenceType named "ContainsElement" for ViewType in order to reference the element indicated by ContainedElements

## ViewType
- Fixed ViewType in order to contain AASReferenceType instances by means of Organizes References in the ContainedElements Folder.

# **Version 0.2.0**

## New ObjectTypes
- Created **ViewType** to map View. Views are used to group Referable entities under an AAS.
- Created **SubmodelElementCollectionType** to map SubmodelElementCollection. It is a subtype of SubmodelElementType;
- Created **ReferenceElementType** to map ReferenceElementType. It is a subtype of DataElementType;
- Created **FileType** to map File. It is a subtype of DataElementType;

## AASType
- Added a new component named **asset** which is an AASReferenceType;
- Since _HasAsset_ is now a NonHierarchical ReferenceType, the InstanceDeclaration related to this Reference disappears from the type. But _HasAsset_ is still used to connect an AASType instance to its AssetType instance.
- Added a component **Views** which is a FolderType used to aggregate Views of the AAS.

## SubmodelType
- Added the component **parent** which is an AASReferenceType;
- **semanticId** now is referenced by an HasComponent Reference instead of an HasSemantic ReferenceType;

## SubmodelElementType
- **semanticId** now is referenced by an HasComponent Reference instead of an HasSemantic ReferenceType;

## ConceptDictionary
- Added a folder **ConceptDescriptions** to organize AASReferenceType instances targeting Conceptdescription;
- The component **category** has been removed;

## DataSpecificationIEC61360Type
- New UA Properties has been defined in order to describe AAS Property on the basis of IEC 61360 attributes. Now an instance of this ObjectType features the following properties:

    | UA Property/Component BrowseName (*=mandatory) | UA DataType or ObjectType |
    -----------------|----------------
    |**identifier***| String|
    |**preferredName***| String|
    |**definition***|String|
    |**dataType***|String|
    |**unit**|String|
    |**unitId**|AASReferenceType|
    |**iecCategory**|String|
    |**iecLanguageCode**|String|
    |**note**|String|
    |**shortName**|String|
    |**valueFormat**|String|
    |**version**|String|
    |**revision**|String|

## ReferenceTypes
- **HasAsset** now is NonHierarchical;
- New NonHierarchical ReferenceType named **HasSubmodel** to connect AASType instances to SubmodelType instances;
- **HasSemantic** now is NonHierarchical and replaces **HasLocalSemantic**;
- **HasSubmodelSemantic** is now NonHierarchical and it is subtype of HasSemantic;
- **IsDerivedFrom** now is NonHierarchical and replaces **IsLocalDerivedFrom**;
- New NonHierarchical ReferenceType named **HasAssetIdentificationModel** to connect AssetType instances to the SubmodelType instance relevant the identification of the Asset. It is subtype of HasSubmodel;
- Removed **IsLocalCaseOf** since there is no useful use case for this referenceType;

## General fixes
- The DataType attribute of all **description** UA Properties has been changed to _LocalizedText_ and the ValueRank attribute has been changed to _OneDimension_. In other word now **description** Property is an Array of LocalizedText;
- In **AASReferenceType**, the BrowseName of UA Property **key** has been changed to **keys**;