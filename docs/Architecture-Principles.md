## Architectural Principles

The MOSIP philisophy is to provide a "Good ID". As part of this MOSIP embraces a core set of design and architecture principles that allow the platform to offer best practices for a Good ID system. MOSIP is built on the following architecture principles

* MOSIP must follow **platform based approach** so that all common features are abstracted as reusable components and frameworks into a common layer
* MOSIP must follow **API first** approach and expose the business functions as RESTful services
* MOSIP must **not use proprietary** or commercial license frameworks. Where deemed essential, such components must be encapsulated to enable their replacement if necessary (to avoid vendor lock-in)
* MOSIP must use **open standards** to expose it’s functionality (to avoid technology lock-in)
* Each MOSIP component must be independently **scalable** (scale out) to meet varying load requirements
* MOSIP must use **commodity computing** hardware & software to build the platform
* Data must be **encrypted** in-flight and at-rest. All requests must be authenticated and authorized. Privacy of Identity Data is an absolute must in MOSIP
* MOSIP must follow the following manageability principles – **Auditability** & monitor ability of every event in the system, testability of every feature of the platform & easy upgrade ability of the platform
* MOSIP must follow the principles of **Zero-Knowledge** which means that the services know nothing about the Personally Identifiable Information (PII) data stored.
* MOSIP components must be **loosely coupled** so that they can be composed to build the identity solution as per the requirements of a country
* MOSIP must support **i18n** capability
* All modules of MOSIP should be resilient such that the solution as a whole is **fault tolerant**
* The key sub-systems of MOSIP should be designed for **extensibility**. For example, if an external system has to be integrated for fingerprint data, it should be easy to do so.

The key design aspects considered for MOSIP are

### Ecosystem approach
The MOSIP platform is a framework and an end-to-end solution needs additional components. For example, biometric devices and ABIS solutions are key to process an individual's data and prove uniqueness. Through a well defined set of standard interfaces MOSIP allows for integration of such components and offers choice of providers for the same. MOSIP also needs to cater to a diverse set of institutions wanting to authenticate an Individual against the data stored in MOSIP.
So, key parameters are
* All public/external facing interfaces of MOSIP must be standards-based for interoperability.
* 3rd party components should be integrated via standard interfaces and offer a provider model where needed. 

### Configurability
MOSIP should be flexible for countries to configure the base platform according to their specific requirements. Some of the examples of configurability are

* Country should be able to choose the features required. For example, it must be possible for a country to turn off Finger Print capture
* Country should be able to configure the attributes of an ID Object
* Country should be able to define the length of the UIN number

### Extensibility
MOSIP should be flexible to extend functionality on top of the basic platform. Some of the examples of extensibility are

* A country should be able to introduce a new step in processing data
* Integrate MOSIP with other ID systems and include it as part of the MOSIP data processing flow

### Modularity
All components in MOSIP should be modular and their features exposed via interfaces such that the implementation behind the interface can be changed without affecting other modules. Some examples of modularity are

* UIN generator algorithm provided by the platform can be replaced by a country with their own implementation
* The default demographic deduplication algorithm provided by MOSIP can be changed to a different one without impacting the process flow
