---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 0f7a05cd0cd711388973c3f823b1aee6aa9f6902
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188932"
---
# <span data-ttu-id="715f1-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="715f1-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="715f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="715f1-102">SYNOPSIS</span></span>
<span data-ttu-id="715f1-103">Ottiene un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="715f1-103">Gets a resource provider.</span></span>

## <span data-ttu-id="715f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="715f1-104">SYNTAX</span></span>

### <span data-ttu-id="715f1-105">ListAvailable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="715f1-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="715f1-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="715f1-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="715f1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="715f1-107">DESCRIPTION</span></span>
<span data-ttu-id="715f1-108">Il cmdlet **Get-AzResourceProvider** ottiene un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="715f1-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="715f1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="715f1-109">EXAMPLES</span></span>

### <span data-ttu-id="715f1-110">Esempio 1: ottenere tutti i provider di risorse registrati con l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="715f1-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="715f1-111">Questo comando consente di ottenere tutti i provider di risorse dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="715f1-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="715f1-112">Esempio 2: ottenere tutti i dettagli del provider di risorse dal ProviderNamespace indicato</span><span class="sxs-lookup"><span data-stu-id="715f1-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="715f1-113">Questo comando consente di ottenere tutti i provider di risorse in "Microsoft. Compute".</span><span class="sxs-lookup"><span data-stu-id="715f1-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="715f1-114">Esempio 3: ottenere tutti i dettagli del provider di risorse dalla matrice ProviderNamespace specificata</span><span class="sxs-lookup"><span data-stu-id="715f1-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="715f1-115">Questo comando consente di ottenere tutti i provider di risorse in "Microsoft. Compute" e "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="715f1-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="715f1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="715f1-116">PARAMETERS</span></span>

### <span data-ttu-id="715f1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="715f1-117">-ApiVersion</span></span>
<span data-ttu-id="715f1-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="715f1-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="715f1-119">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="715f1-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715f1-120">-DefaultProfile</span></span>
<span data-ttu-id="715f1-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="715f1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="715f1-122">-ListAvailable</span></span>
<span data-ttu-id="715f1-123">Indica che questa operazione ottiene tutti i provider di risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="715f1-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="715f1-124">-Location</span></span>
<span data-ttu-id="715f1-125">Specifica la posizione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="715f1-125">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="715f1-126">-Pre</span></span>
<span data-ttu-id="715f1-127">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="715f1-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="715f1-128">-ProviderNamespace</span></span>
<span data-ttu-id="715f1-129">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="715f1-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715f1-130">CommonParameters</span></span>
<span data-ttu-id="715f1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715f1-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="715f1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715f1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="715f1-133">INPUTS</span></span>

### <span data-ttu-id="715f1-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="715f1-134">System.String[]</span></span>

## <span data-ttu-id="715f1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="715f1-135">OUTPUTS</span></span>

### <span data-ttu-id="715f1-136">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="715f1-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="715f1-137">Note</span><span class="sxs-lookup"><span data-stu-id="715f1-137">NOTES</span></span>

## <span data-ttu-id="715f1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="715f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="715f1-139">Registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="715f1-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="715f1-140">Annullamento della registrazione-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="715f1-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)

