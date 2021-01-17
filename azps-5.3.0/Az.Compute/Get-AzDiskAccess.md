---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488527"
---
# <span data-ttu-id="6aff5-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6aff5-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="6aff5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6aff5-102">SYNOPSIS</span></span>
<span data-ttu-id="6aff5-103">Ottiene le proprietà degli accessi su disco</span><span class="sxs-lookup"><span data-stu-id="6aff5-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="6aff5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6aff5-104">SYNTAX</span></span>

### <span data-ttu-id="6aff5-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6aff5-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aff5-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aff5-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aff5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aff5-107">DESCRIPTION</span></span>
<span data-ttu-id="6aff5-108">Il cmdlet **Get-AzDiskAccess** ottiene le proprietà degli accessi su disco</span><span class="sxs-lookup"><span data-stu-id="6aff5-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="6aff5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6aff5-109">EXAMPLES</span></span>

### <span data-ttu-id="6aff5-110">Esempio 1: uso del set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="6aff5-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="6aff5-111">Questo comando consente di ottenere le proprietà di una risorsa di Access su disco denominata "DiskAccess01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6aff5-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6aff5-112">Esempio 2: Get-AzDiskAccess per gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6aff5-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="6aff5-113">Questo comando consente di ottenere le proprietà di tutti gli accessi su disco nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6aff5-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="6aff5-114">Esempio 3: ottenere l'accesso a tutti i dischi</span><span class="sxs-lookup"><span data-stu-id="6aff5-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="6aff5-115">Questo comando consente di ottenere le proprietà di tutti gli accessi al disco sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6aff5-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="6aff5-116">Esempio 4: ottenere l'accesso a tutti i dischi usando il carattere jolly</span><span class="sxs-lookup"><span data-stu-id="6aff5-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="6aff5-117">Questo comando consente di ottenere le proprietà di tutti gli accessi al disco sotto il nome dell'abbonamento a partire da "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="6aff5-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="6aff5-118">Esempio 5: ottenere l'accesso al disco usando ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6aff5-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="6aff5-119">Questo comando consente di ottenere le proprietà di un accesso su disco con il ResourceId indicato.</span><span class="sxs-lookup"><span data-stu-id="6aff5-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="6aff5-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6aff5-120">PARAMETERS</span></span>

### <span data-ttu-id="6aff5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aff5-121">-DefaultProfile</span></span>
<span data-ttu-id="6aff5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6aff5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aff5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6aff5-123">-Name</span></span>
<span data-ttu-id="6aff5-124">Specifica il nome di un accesso su disco.</span><span class="sxs-lookup"><span data-stu-id="6aff5-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6aff5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aff5-125">-ResourceGroupName</span></span>
<span data-ttu-id="6aff5-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6aff5-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6aff5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aff5-127">-ResourceId</span></span>
<span data-ttu-id="6aff5-128">ID risorsa per l'accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="6aff5-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aff5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aff5-129">CommonParameters</span></span>
<span data-ttu-id="6aff5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aff5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aff5-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aff5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aff5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6aff5-132">INPUTS</span></span>

### <span data-ttu-id="6aff5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6aff5-133">System.String</span></span>

## <span data-ttu-id="6aff5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6aff5-134">OUTPUTS</span></span>

### <span data-ttu-id="6aff5-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6aff5-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="6aff5-136">Note</span><span class="sxs-lookup"><span data-stu-id="6aff5-136">NOTES</span></span>

## <span data-ttu-id="6aff5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6aff5-137">RELATED LINKS</span></span>
