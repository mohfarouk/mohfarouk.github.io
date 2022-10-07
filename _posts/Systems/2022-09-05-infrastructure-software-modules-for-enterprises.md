---
layout: post
title:  "Infrastructure Software Modules for Enterprises"
date:   2022-09-05
categories: PM
premalink: "infrastructure-software-modules-for-enterprises" 
---

# Infrastructure Software Modules for Enterprises
![Infrastructure Software Modules for Enterprises](https://media-exp1.licdn.com/dms/image/C5612AQH1otuJQlMRgA/article-cover_image-shrink_423_752/0/1644955988475?e=1670457600&v=beta&t=9gcWqU6tA-yQOtZos32-3RN7WJYUsK635CpOZ1kXMRg)

## Overview 
There are common functionalities among software systems that make them flexible for administration and tracking. These functionalities can be considered as an infrastructure for any software system and can be organized into modules, which we will call infrastructure modules. These modules provide common functionalities to users and to other modules that handle business operations in an enterprise.

This article consists of three sections 
- Types of Software Modules
- Infrastructure Modules 
- Dependency and Extendibility

## Types of Software Modules
In every software system, there are two types of modules 

1. **Business Modules**: These are software modules developed to allow the organization to perform its business (either internal or external). For example, some Enterprise Resource Planning (ERP) modules are considered internal business for the organization. Public services provided to citizens, external organizations, or integrated systems are considered external business.
2. **Infrastructure Modules**: These are software modules developed to control how the system will work by providing rules for conducting the business. System admins can manage infrastructure modules to provide flexibility regarding how the software system works and to adapt to required changes in the system.

![Types of Software Modules](https://media-exp1.licdn.com/dms/image/C5612AQElCYmg9p1d3w/article-inline_image-shrink_1000_1488/0/1644954475091?e=1670457600&v=beta&t=cFm-_uw0o6RAt3TOE7wRp6JY-frWymRsF6kVnslBxXs)

Infrastructure modules are the core of the system and are independent of the business functionality. They exist as a base on which the business modules are built.

## Infrastructure Modules 
Below diagram shows the main infrastructure modules described in this article. These modules are like building blocks for the infrastructure layer. Every module provides a set of functionalities to support the business modules that will be implemented in the system.

![](https://media-exp1.licdn.com/dms/image/C5612AQE_HacK7DTosQ/article-inline_image-shrink_1000_1488/0/1644954279490?e=1670457600&v=beta&t=5ZMKhJlGmegB_dDFBQJur47Ov8LWgVJj8opsOmUUp30)

### Localization Module
The Localization module manages texts and their translations that will be displayed to the system’s users. In countries where English is not the main language, almost every software system will need to be bilingual. In some cases, it may need to be multilingual. 

One scenario in which the multilingual software is required is when the organization that owns the software system has foreign employees. These employees need to interact with the system in a language other than the local language. This other language may be English or any suitable language supported by the system. Another scenario is when there is a need to generate reports from the system in foreign languages to be used outside the country. Supporting multiple languages in a software system is known as localization.

### Lookups Module
When filling data form in the system, in some cases the user will need to select some items from a list. This selection can be single selection or multiple selection. Lists that consist of singular items (that is, the item consists of only a name) are called lookups.

Lookups items can be modifiable or non-modifiable. The Lookups module manages these lists and allows adding, editing, or deleting the items in the list.

### Persons Module
Every organization’s system needs to store and manage persons’ data. One person in the system may have multiple roles. For example, a person can be an employee, investor, student, and so on. The system should not repeat the person data. 

The Persons module manages persons’ data and allows adding, editing, or deleting persons. In addition, it prevents the repetition of the persons’ data in the system by storing the shared person data in the person entity instead of having multiple entities per role and repeating the person’s data with each entity. The data that related to the person’s role can be managed by extensions.

### Organization Structure Module
Almost any organization consists of departments organized in a hierarchy called the organization structure. Every department contains positions filled by employees. Positions also have a hierarchy called a reporting hierarchy. The Organization Structure module manages the departments and their hierarchies as well as the positions and their reporting hierarchies. This module also enables assigning persons to positions to become employees.

### Authentication Module
Persons who will use the system need to be authenticated by the system in order to recognize them, and before authentication, users need to register with the system. Registration can be done via information the person knows (for example, password, username and password, email and password, or mobile number and password) or things the person has (device, ID card, physical token) or via something physical about the person (for example, fingerprint, voice, eye, or face). The registration information can involve a combination of these things.

Based on the registration methods, the system will allow the person to select how to be authenticated and will compare the entered information with the registered information to authenticate the user. The Authentication module manages the registration information and the authentication methods for the persons who use the system.

### Authorization Module
Every system provides business services to its users. A service can be requested or used by persons who have permission to access it. It is also possible for a service to be accessed by persons who belong to an entity that has permission to access the services. The Authorization module manages defining the roles and groups and assigning persons or departments to them. In addition, the Authorization module manages the permissions given to the entities by allowing or denying the services.

### Communication Rules Module
Some organizations have communication rules among positions (employees) or departments. For example, employees are allowed to communicate with their peers, their supervisors, their manager, and their supervised employees. Sometimes there are exceptions in the communication rules. For example, a group of selected employees can communicate with all employees in the organization. Communication rules help in assigning tasks to employees by other employees or in writing correspondence to other employees.

The Communication Rules module manages who can communicate with whom by allowing adding, editing, or deleting the rules.

### Tasks Module
Every person who uses the system may be required to perform a task. The person’s task can be created by the person or assigned to them by another person or by the system. 

The Tasks module enables the persons to manage their tasks. Persons can use this module to view, create, or complete their tasks. It also allows persons to assign tasks to other persons (delegation) based on the defined communication rules and allow them to monitor the progress of the tasks.

### Workflows Module
All systems require workflow to perform a business process. A business process is the steps required to provide a service to person or to another organization. Some services provided by the system have an application form that can be filled out manually by persons who use the system or filled automatically by the system or by an integrated system. The application form then goes through steps (tasks) assigned to persons who are responsible for performing these steps. After all steps are completed, the service’s application is considered completed. It may be rejected or approved. In case of approval, the system modifies its state based on the action associated with the service.

The Workflow module manages the definition of the service’s application, workflow steps and routing, and assigning tasks to responsible persons. It also invokes the required actions to complete the workflow.

### Notifications Module
The organization may need to send notification messages to persons who use the system. And persons who use the system may need to receive notifications when changes happened on the system. Notification messages are sent using the preferred notification method for the persons (for example, SMS, mobile, or web notification).

The Notifications module allows users to define their notification preferences and be able to view their notifications. It also allows a system admin to define the default method and enable or disable some methods. And it tracks notifications until they are sent to their destinations.

### Follow-Up Module
The users of the system may need to follow up an object in the system (workflow instance, task, invoice, payment order, and so on). The Follow-Up module allows the user to select an object and create, modify, or delete the follow-up for this object. The Follow-Up module uses the Notification module to notify the user.

### Documents Module
Any software system will require attaching documents based on business functionality. Users of the system should include the attached document information while attaching the document. Document information could be the document type, issue date, notes, and object the document is related to (based on the context where the document is attached—for example, the document may be related to a person, company, invoice, or something else).

The Documents module manages the attached documents by collecting the required information when the users attach documents, providing the ability to search the attached documents, and viewing versions of the attached documents. It also manages the attached documents by providing the ability to search.

### Payments Module
As mentioned, organizations provide services, and services can be internal for employees or external for clients. Services often have fees that must be paid. There are many methods to collect payments. For example, payment can be done by any of the following:
- Cash
- Check
- Bank transfer
- POS device
- Online payment gateway
- PayPal or similar services
- Money collection service providers

This means money can be collected online, on the organization premises, or by a partner providing a money collection service. In some cases, paid money can be refunded.

The Payment module allows users to perform the payment operation using the payment methods enabled by the organization, search and view payments registered in the system, and request refunds.

### Signatures Module
The Signatures module manages the operations of validating attached digitally signed documents and generating digitally or electronically signed documents. There are two types of signatures: digital and electronic. Digital signature involves hashing and encrypting data by the private key of the person or organization who signs the data. Electronic signature involves appending the image of the signature of the person who signs the data.

Documents generated by other organization and imported to the system (attached to the system by the users) can be digitally signed. If the system is expecting to receive digitally signed documents, the system will verify those signed documents to ensure their validity.

Documents generated by the system and provided to other organizations (such as reports, certificates, letters, and so forth) can be electronically signed and/or digitally signed.

Using signatures with internal operations inside the organization is not recommended because it adds additional unnecessary effort (though some organizations do ask to include signature in their internal operations).

## Dependency and Extendibility
Dependency exists among infrastructure modules. In other words, some modules need to be implemented first before the other modules can be implemented. In addition, infrastructure modules should be extendable to support the business modules that may use them. Plugins can be used to extend the functionality of the infrastructure modules. 

### Dependency
The dependency among infrastructure modules is illustrated in the below figure. On the left side of the figure appear three modules that are shared with the other modules. On the right side are the remaining modules that depend on the shared modules.

![Dependency](https://media-exp1.licdn.com/dms/image/C4D12AQHqVC45FrBy5w/article-inline_image-shrink_1000_1488/0/1644861821867?e=1670457600&v=beta&t=44qkh4QpeFJsLCKraPsHGzCFGFMSOzxpgi48Ygjlc7o)

### Extendibility
Every infrastructure (or business) module has extension points in order to be integrated with other modules, either business modules or infrastructure modules. The modules that use these extension points implement plugins to be connected to the extension points. The below figure shows a module that has connection points and plugins.

![](https://media-exp1.licdn.com/dms/image/C4D12AQHHQegeSD3Qug/article-inline_image-shrink_1000_1488/0/1644861777630?e=1670457600&v=beta&t=Tw0H9DEvSEafSquHyzyk1z132upn9CdasiN0eQlW82I)

As an example, the next figure shows that the Authorization module has extension points for the business modules to enable the business modules to provide lists of services and to be included in the Authorization module. This will enable those business services to be configured and will let them be used by the Authorization module, which will manage the authorization of users on these services.

![](https://media-exp1.licdn.com/dms/image/C4D12AQFlsuvp96dRuw/article-inline_image-shrink_1000_1488/0/1644861791632?e=1670457600&v=beta&t=CcF59eCi7vtV9hiaarZw8KGn9-RBH1XMGZWXSHfT0uo)

<br/>

---

<br/>
If you are interested to know more, you can refer to my book Infrastructure Software Modules for Enterprises. It contains description of all modules and provide use-cases, wireframes, and entities relations.

[![Infrastructure Software Modules for Enterprises](https://m.media-amazon.com/images/I/41wOgqP+LyL._SX328_BO1,204,203,200_.jpg)](https://www.amazon.com/Infrastructure-Software-Modules-Enterprises-Wireframes/dp/1484230205){:target="_blank"} 