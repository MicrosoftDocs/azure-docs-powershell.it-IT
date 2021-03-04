---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: f2f18ac77f923247f2bef0e78802a2f05cf302d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954541"
---
# <span data-ttu-id="6d676-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="6d676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d676-102">SYNOPSIS</span></span>
<span data-ttu-id="6d676-103">Ottiene una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="6d676-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="6d676-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d676-104">SYNTAX</span></span>

### <span data-ttu-id="6d676-105">GetByResourceNameNoExpandParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d676-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d676-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d676-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d676-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d676-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d676-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d676-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d676-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d676-109">DESCRIPTION</span></span>
<span data-ttu-id="6d676-110">Il cmdlet **Get-AzNetworkProfile** recupera una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="6d676-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="6d676-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d676-111">EXAMPLES</span></span>

### <span data-ttu-id="6d676-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d676-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="6d676-113">In questo modo viene recuperato il profilo di rete np1 nel gruppo di risorse rg1</span><span class="sxs-lookup"><span data-stu-id="6d676-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="6d676-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d676-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="6d676-115">Vengono recuperati i profili di rete che iniziano con "np"</span><span class="sxs-lookup"><span data-stu-id="6d676-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="6d676-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d676-116">PARAMETERS</span></span>

### <span data-ttu-id="6d676-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-117">-DefaultProfile</span></span>
<span data-ttu-id="6d676-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d676-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d676-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6d676-119">-ExpandResource</span></span>
<span data-ttu-id="6d676-120">Riferimento di risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="6d676-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d676-121">-Name</span></span>
<span data-ttu-id="6d676-122">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="6d676-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6d676-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d676-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d676-124">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="6d676-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6d676-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d676-125">-ResourceId</span></span>
<span data-ttu-id="6d676-126">ID manager delle risorse di Azure del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="6d676-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d676-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d676-127">CommonParameters</span></span>
<span data-ttu-id="6d676-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d676-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d676-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d676-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d676-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d676-130">INPUTS</span></span>

### <span data-ttu-id="6d676-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6d676-131">System.String</span></span>

## <span data-ttu-id="6d676-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d676-132">OUTPUTS</span></span>

### <span data-ttu-id="6d676-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="6d676-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d676-134">NOTES</span></span>

## <span data-ttu-id="6d676-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d676-135">RELATED LINKS</span></span>

[<span data-ttu-id="6d676-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="6d676-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="6d676-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d676-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
