CoreAAS
=======
This project is an implementation of the Platform Industrie 4.0 Asset Administration Shell (AAS) metamodel in OPC UA. It defines an open Information Model defining the main parts of the AAS metamodel. This Information is based on the version 2.1 of the AAS metamodel.

The project is still work in progress and all the main components already defined will be tracked in the table at the end of this document.

CoreAAS is implemented in [node-opcua-coreaas](https://github.com/OPCUAUniCT/node-opcua-coreaas), an extension of the OPC UA SDK for Node.js [node-opcua](https://github.com/node-opcua/node-opcua).

## Overview
For Industrie 4.0, an asset is any "object which has a value for an organization". Thus,assets in Industrie 4.0 can take almost any form, for example be a production system, a product, a software installation, intellectual properties or even human resources.

Assets shall have a logical representation in the "information world", for example shall be managed by IT-systems. Thus, an asset has to be precisely identified as an entity, shall have a "specific state within its life (at least a type or instance)", shall have communication capabilities, shall be represented by means of information and shall be able to provide technical functionality. This logical representation of an asset is called Administration Shell. The combination of asset and Administration Shell forms the so-called I4.0 Component.

You can look into metamodel using software like [UAModeler](https://www.unified-automation.com/products/development-tools/uamodeler.html) from Unified Automation GmbH. The xml file in models folder can be easily imported in every OPC UA SDK allowing information model xml file to be imported.

More information are available on the [wiki](https://github.com/OPCUAUniCT/coreAAS/wiki).

An implementation of CoreAAS is available [here](https://github.com/OPCUAUniCT/node-opcua-coreaas). It is an extension for [node-opcua](https://github.com/node-opcua/node-opcua), an OPC UA Stack for Node.js.

---

The foundation of coreAAS is the AAS metamodel defined in [this](https://www.plattform-i40.de/PI40/Redaktion/DE/Downloads/Publikation/Details-of-the-Asset-Administration-Shell-Part1.html) document.

## AAS metamodel entities tracking
The following table shows which AAS metamodel entities are already mapped in coreAAS metamodel.

Status legend:
Implementation complete :white_check_mark:

Not implemented :x:

Under construction :construction:

Unstable (incomplete or bugged) :warning:

| AAS Metamodel Entity  | Status |
| ------------- | ------------- |
| AssetAdministrationShell  | :white_check_mark:  |
| Asset  | :white_check_mark:  |
| Submodel  | :white_check_mark:  |
| SubmodelElement  | :white_check_mark:  |
| DataElement  | :white_check_mark:  |
| Property  | :white_check_mark:  |
| MultiLanguageProperty  | :x:  |
| Range  | :white_check_mark:  |
| File  | :white_check_mark:  |
| Blob  | :x:  |
| ReferenceElement  | :white_check_mark:  |
| Capability  | :white_check_mark:  |
| SubmodelElementCollection  | :white_check_mark:  |
| RelationshipElement  | :white_check_mark:  |
| Operation  | :x:  |
| OperationVariable  | :x:  |
| Event  | :x:  |
| Entity  | :white_check_mark:  |
| View  | :white_check_mark:  |
| ConceptDictionary  | :white_check_mark:  |
| ConceptDescription  | :white_check_mark:  |
| Reference  | :white_check_mark:  |
| Key  | :white_check_mark:  |
| DataSpecification  | :white_check_mark:  |
| DataSpecificationContent  | :white_check_mark:  |
| DataSpecificationIEC61360  | :white_check_mark:  |
