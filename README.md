# City Places API

REST API for managing a catalog of city cafes and places, built with ASP.NET Core (.NET 10) following Clean Architecture principles.

## Domain Mapping

| Role in Requirements | Domain Entity / Object | Description |
| :--- | :--- | :--- |
| **Main entity** | `Place` | A cafe or city place (unique title) |
| **Group entity** | `Feature` | A feature or tag of a place (e.g., *Pet-friendly*, *Terrace*, *Generator*; unique name) |
| **Link entity** | `PlaceFeature` | Many-to-many join table between `Place` and `Feature` |
| **Attachment entity** | `PlaceAttachment` | Uploaded photo of the place/interior |
| **Attributes value object** | `PlaceDetails` | Owned JSONB object (`Address`, `AverageCheck`, `WorkingHours`) |