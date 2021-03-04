---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969357"
---
# <span data-ttu-id="a4a4d-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a4a4d-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="a4a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a4d-103">Ottiene le proprietà di Accesso al disco</span><span class="sxs-lookup"><span data-stu-id="a4a4d-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="a4a4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4a4d-104">SYNTAX</span></span>

### <span data-ttu-id="a4a4d-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a4a4d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4a4d-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4a4d-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a4d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4a4d-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a4d-108">Il cmdlet **Get-AzDiskAccess** ottiene le proprietà degli accessi al disco</span><span class="sxs-lookup"><span data-stu-id="a4a4d-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="a4a4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4a4d-109">EXAMPLES</span></span>

### <span data-ttu-id="a4a4d-110">Esempio 1: Uso del set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="a4a4d-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="a4a4d-111">Questo comando ottiene le proprietà di una risorsa Accesso disco denominata 'DiskAccess01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a4a4d-112">Esempio 2: Get-AzDiskAccess per gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a4a4d-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="a4a4d-113">Questo comando ottiene le proprietà di tutti gli accessi al disco nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="a4a4d-114">Esempio 3: Ottenere tutto l'accesso al disco</span><span class="sxs-lookup"><span data-stu-id="a4a4d-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="a4a4d-115">Questo comando ottiene le proprietà di tutti gli accessi al disco nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="a4a4d-116">Esempio 4: Ottenere tutto l'accesso al disco usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="a4a4d-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="a4a4d-117">Questo comando recupera le proprietà di tutti gli accessi al disco sotto il nome dell'abbonamento a partire da "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="a4a4d-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="a4a4d-118">Esempio 5: Ottenere l'accesso al disco con ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="a4a4d-119">Questo comando ottiene le proprietà di un accesso a disco con il valore ResourceId specificato.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="a4a4d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4a4d-120">PARAMETERS</span></span>

### <span data-ttu-id="a4a4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a4d-121">-DefaultProfile</span></span>
<span data-ttu-id="a4a4d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a4d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a4a4d-123">-Name</span></span>
<span data-ttu-id="a4a4d-124">Specifica il nome di un accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="a4a4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4a4d-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a4a4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4a4d-127">-ResourceId</span></span>
<span data-ttu-id="a4a4d-128">ID risorsa per l'accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="a4a4d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a4d-129">CommonParameters</span></span>
<span data-ttu-id="a4a4d-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a4d-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4a4d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a4d-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4a4d-132">INPUTS</span></span>

### <span data-ttu-id="a4a4d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a4a4d-133">System.String</span></span>

## <span data-ttu-id="a4a4d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4a4d-134">OUTPUTS</span></span>

### <span data-ttu-id="a4a4d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a4a4d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="a4a4d-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4a4d-136">NOTES</span></span>

## <span data-ttu-id="a4a4d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4a4d-137">RELATED LINKS</span></span>
