---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187127"
---
# <span data-ttu-id="2577d-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="2577d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2577d-102">SYNOPSIS</span></span>
<span data-ttu-id="2577d-103">Ottiene una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="2577d-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="2577d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2577d-104">SYNTAX</span></span>

### <span data-ttu-id="2577d-105">GetByResourceNameNoExpandParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2577d-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2577d-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2577d-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2577d-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2577d-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2577d-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2577d-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2577d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2577d-109">DESCRIPTION</span></span>
<span data-ttu-id="2577d-110">Il cmdlet **Get-AzNetworkProfile** recupera una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="2577d-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="2577d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2577d-111">EXAMPLES</span></span>

### <span data-ttu-id="2577d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2577d-112">Example 1</span></span>
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

<span data-ttu-id="2577d-113">In questo modo viene recuperato il profilo di rete np1 nel gruppo di risorse rg1</span><span class="sxs-lookup"><span data-stu-id="2577d-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="2577d-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2577d-114">Example 2</span></span>
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

<span data-ttu-id="2577d-115">Vengono recuperati i profili di rete che iniziano con "np"</span><span class="sxs-lookup"><span data-stu-id="2577d-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="2577d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2577d-116">PARAMETERS</span></span>

### <span data-ttu-id="2577d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-117">-DefaultProfile</span></span>
<span data-ttu-id="2577d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2577d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2577d-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2577d-119">-ExpandResource</span></span>
<span data-ttu-id="2577d-120">Riferimento di risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="2577d-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="2577d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2577d-121">-Name</span></span>
<span data-ttu-id="2577d-122">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2577d-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="2577d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2577d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2577d-124">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2577d-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="2577d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2577d-125">-ResourceId</span></span>
<span data-ttu-id="2577d-126">ID manager delle risorse di Azure del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2577d-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="2577d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2577d-127">CommonParameters</span></span>
<span data-ttu-id="2577d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2577d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2577d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2577d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2577d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="2577d-130">INPUTS</span></span>

### <span data-ttu-id="2577d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2577d-131">System.String</span></span>

## <span data-ttu-id="2577d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2577d-132">OUTPUTS</span></span>

### <span data-ttu-id="2577d-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="2577d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="2577d-134">NOTES</span></span>

## <span data-ttu-id="2577d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2577d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2577d-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="2577d-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="2577d-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2577d-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
