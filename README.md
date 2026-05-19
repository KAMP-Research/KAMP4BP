# KAMP4BP

KAMP4BP extends KAMP for business-process models. It connects process-oriented artefacts with Palladio Component Model (PCM) concepts and provides EMF models, generated editors, field-of-activity annotations, and business-process-specific modification marks.

## Installation

Install KAMP4BP from the KAMP update-site page:

```text
https://kamp-research.github.io/KAMP/kamp4bp/
```

For a complete setup, use the composite update site instead:

```text
https://kamp-research.github.io/KAMP/all/
```

In Eclipse, open `Help > Install New Software...`, paste the update-site URL into `Work with`, select the KAMP4BP feature, and finish the wizard. Restart Eclipse after installation.

## Dependencies

KAMP4BP depends on the KAMP and Palladio modelling stack:

- KAMP core for base modification marks and change-propagation infrastructure.
- Eclipse Modeling Framework (EMF), EMF.Edit, and generated EMF editor support.
- Palladio Component Model (PCM), including usage-model and repository concepts referenced by the business-process model.
- Palladio build dependencies from the Palladio 5.2.1 update sites.
- Eclipse Platform/PDE dependencies from the Eclipse 2023-03 target.

## Domain

KAMP4BP targets business processes, organizational environments, data objects, device resources, actor resources, and workloads. It is intended for analysing how process, role, data, or resource changes affect business-process-related models and downstream work items.

## Important Models

- `bp.ecore`: PCM-related business-process extensions. Important elements include `ActorStep`, `Activity`, `ProcessWorkload`, `ProcessTriggerPeriod`, `AcquireDeviceResourceAction`, `ReleaseDeviceResourceAction`, `OrganizationEnvironmentModel`, `Role`, `ActorResource`, `DeviceResource`, `WorkingPeriod`, `DataObject`, `CollectionDataObject`, `CompositeDataObject`, and `DataModel`.
- `BPFieldOfActivityAnnotations.ecore`: annotations for business-process-specific field-of-activity information such as user action annotations, goods, messages, organizational units, training courses, and process specifications.
- `BPModificationmarks.ecore`: modification marks such as `BPSeedModifications`, `BPInterBusinessProcessPropagation`, `BPModifyDataObject`, `BPModifyActorStep`, `BPModifyEntryLevelSystemCall`, `BPModifyDeviceResource`, and `BPModifyRole`.

## Usage

Model business processes and their organizational/data context with the provided EMF editors. Represent relevant changes as BP modification marks and use KAMP's change-propagation workflow to derive affected process elements and follow-up activities.

KAMP4BP is most useful when process models are maintained together with PCM architecture and usage models, because the BP model references PCM concepts and extends them with process-specific information.
