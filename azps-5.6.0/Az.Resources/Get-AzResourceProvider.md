---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 57e1aa691ffaca498e925488fb90fb8b828ff9f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959470"
---
# <span data-ttu-id="c299f-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c299f-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="c299f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c299f-102">SYNOPSIS</span></span>
<span data-ttu-id="c299f-103">Ottiene un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c299f-103">Gets a resource provider.</span></span>

## <span data-ttu-id="c299f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c299f-104">SYNTAX</span></span>

### <span data-ttu-id="c299f-105">ListAvailable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c299f-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c299f-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="c299f-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c299f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c299f-107">DESCRIPTION</span></span>
<span data-ttu-id="c299f-108">Il cmdlet **Get-AzResourceProvider** ottiene un provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c299f-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="c299f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c299f-109">EXAMPLES</span></span>

### <span data-ttu-id="c299f-110">Esempio 1: Ottenere tutti i provider di risorse registrati con l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="c299f-110">Example 1: Get all resource providers registered with the current subscription</span></span>

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

<span data-ttu-id="c299f-111">Questo comando recupera tutti i provider di risorse dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c299f-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="c299f-112">Esempio 2: Ottenere tutti i dettagli del provider di risorse dal provider Di provider specificato</span><span class="sxs-lookup"><span data-stu-id="c299f-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

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

<span data-ttu-id="c299f-113">Questo comando recupera tutti i provider di risorse in "Microsoft.Compute".</span><span class="sxs-lookup"><span data-stu-id="c299f-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="c299f-114">Esempio 3: Ottenere tutti i dettagli del provider di risorse dalla matrice ProviderNtassi specificata</span><span class="sxs-lookup"><span data-stu-id="c299f-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

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

<span data-ttu-id="c299f-115">Questo comando recupera tutti i provider di risorse in "Microsoft.Compute" e "Microsoft.Network".</span><span class="sxs-lookup"><span data-stu-id="c299f-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="c299f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c299f-116">PARAMETERS</span></span>

### <span data-ttu-id="c299f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c299f-117">-ApiVersion</span></span>
<span data-ttu-id="c299f-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c299f-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c299f-119">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="c299f-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c299f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c299f-120">-DefaultProfile</span></span>
<span data-ttu-id="c299f-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c299f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c299f-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c299f-122">-ListAvailable</span></span>
<span data-ttu-id="c299f-123">Indica che questa operazione ottiene tutti i provider di risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="c299f-123">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="c299f-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c299f-124">-Location</span></span>
<span data-ttu-id="c299f-125">Specifica la posizione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c299f-125">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="c299f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="c299f-126">-Pre</span></span>
<span data-ttu-id="c299f-127">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c299f-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c299f-128">-Provider Provider</span><span class="sxs-lookup"><span data-stu-id="c299f-128">-ProviderNamespace</span></span>
<span data-ttu-id="c299f-129">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c299f-129">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="c299f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c299f-130">CommonParameters</span></span>
<span data-ttu-id="c299f-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c299f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c299f-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c299f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c299f-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c299f-133">INPUTS</span></span>

### <span data-ttu-id="c299f-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c299f-134">System.String[]</span></span>

## <span data-ttu-id="c299f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c299f-135">OUTPUTS</span></span>

### <span data-ttu-id="c299f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c299f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="c299f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c299f-137">NOTES</span></span>

## <span data-ttu-id="c299f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c299f-138">RELATED LINKS</span></span>

[<span data-ttu-id="c299f-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c299f-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="c299f-140">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c299f-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


