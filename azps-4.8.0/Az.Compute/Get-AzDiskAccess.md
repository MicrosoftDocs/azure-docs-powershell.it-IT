---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031611"
---
# <span data-ttu-id="5928a-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5928a-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="5928a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5928a-102">SYNOPSIS</span></span>
<span data-ttu-id="5928a-103">Ottiene le proprietà degli accessi su disco</span><span class="sxs-lookup"><span data-stu-id="5928a-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="5928a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5928a-104">SYNTAX</span></span>

### <span data-ttu-id="5928a-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5928a-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5928a-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="5928a-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5928a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5928a-107">DESCRIPTION</span></span>
<span data-ttu-id="5928a-108">Il cmdlet **Get-AzDiskAccess** ottiene le proprietà degli accessi su disco</span><span class="sxs-lookup"><span data-stu-id="5928a-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="5928a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5928a-109">EXAMPLES</span></span>

### <span data-ttu-id="5928a-110">Esempio 1: uso del set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="5928a-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="5928a-111">Questo comando consente di ottenere le proprietà di una risorsa di Access su disco denominata "DiskAccess01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5928a-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5928a-112">Esempio 2: Get-AzDiskAccess per gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5928a-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="5928a-113">Questo comando consente di ottenere le proprietà di tutti gli accessi su disco nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5928a-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="5928a-114">Esempio 3: ottenere l'accesso a tutti i dischi</span><span class="sxs-lookup"><span data-stu-id="5928a-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="5928a-115">Questo comando consente di ottenere le proprietà di tutti gli accessi al disco sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5928a-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="5928a-116">Esempio 4: ottenere l'accesso a tutti i dischi usando il carattere jolly</span><span class="sxs-lookup"><span data-stu-id="5928a-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="5928a-117">Questo comando consente di ottenere le proprietà di tutti gli accessi al disco sotto il nome dell'abbonamento a partire da "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="5928a-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="5928a-118">Esempio 5: ottenere l'accesso al disco usando ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5928a-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="5928a-119">Questo comando consente di ottenere le proprietà di un accesso su disco con il ResourceId indicato.</span><span class="sxs-lookup"><span data-stu-id="5928a-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="5928a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5928a-120">PARAMETERS</span></span>

### <span data-ttu-id="5928a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5928a-121">-DefaultProfile</span></span>
<span data-ttu-id="5928a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5928a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5928a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5928a-123">-Name</span></span>
<span data-ttu-id="5928a-124">Specifica il nome di un accesso su disco.</span><span class="sxs-lookup"><span data-stu-id="5928a-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="5928a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5928a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5928a-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5928a-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5928a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5928a-127">-ResourceId</span></span>
<span data-ttu-id="5928a-128">ID risorsa per l'accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="5928a-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="5928a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5928a-129">CommonParameters</span></span>
<span data-ttu-id="5928a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5928a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5928a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5928a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5928a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5928a-132">INPUTS</span></span>

### <span data-ttu-id="5928a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5928a-133">System.String</span></span>

## <span data-ttu-id="5928a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5928a-134">OUTPUTS</span></span>

### <span data-ttu-id="5928a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5928a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="5928a-136">Note</span><span class="sxs-lookup"><span data-stu-id="5928a-136">NOTES</span></span>

## <span data-ttu-id="5928a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5928a-137">RELATED LINKS</span></span>
