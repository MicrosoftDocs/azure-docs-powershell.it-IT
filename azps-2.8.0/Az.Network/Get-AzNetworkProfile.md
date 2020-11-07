---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 1f57a8a9cc65ab9ff4955d6d11e6f4c1a91c417e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853705"
---
# <span data-ttu-id="2e6d1-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="2e6d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6d1-103">Ottiene una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="2e6d1-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="2e6d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e6d1-104">SYNTAX</span></span>

### <span data-ttu-id="2e6d1-105">GetByResourceNameNoExpandParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e6d1-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e6d1-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6d1-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6d1-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6d1-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e6d1-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6d1-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e6d1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e6d1-109">DESCRIPTION</span></span>
<span data-ttu-id="2e6d1-110">Il cmdlet **Get-AzNetworkProfile** recupera una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="2e6d1-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="2e6d1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e6d1-111">EXAMPLES</span></span>

### <span data-ttu-id="2e6d1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e6d1-112">Example 1</span></span>
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

<span data-ttu-id="2e6d1-113">In questo articolo viene recuperato il profilo di rete NP1 nel gruppo di risorse RG1</span><span class="sxs-lookup"><span data-stu-id="2e6d1-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="2e6d1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2e6d1-114">Example 2</span></span>
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

<span data-ttu-id="2e6d1-115">In questo articolo vengono recuperati i profili di rete che iniziano con "NP"</span><span class="sxs-lookup"><span data-stu-id="2e6d1-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="2e6d1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e6d1-116">PARAMETERS</span></span>

### <span data-ttu-id="2e6d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-117">-DefaultProfile</span></span>
<span data-ttu-id="2e6d1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6d1-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2e6d1-119">-ExpandResource</span></span>
<span data-ttu-id="2e6d1-120">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="2e6d1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e6d1-121">-Name</span></span>
<span data-ttu-id="2e6d1-122">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="2e6d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e6d1-124">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="2e6d1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e6d1-125">-ResourceId</span></span>
<span data-ttu-id="2e6d1-126">ID di gestione risorse di Azure del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="2e6d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6d1-127">CommonParameters</span></span>
<span data-ttu-id="2e6d1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6d1-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e6d1-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6d1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e6d1-130">INPUTS</span></span>

### <span data-ttu-id="2e6d1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6d1-131">System.String</span></span>

## <span data-ttu-id="2e6d1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e6d1-132">OUTPUTS</span></span>

### <span data-ttu-id="2e6d1-133">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="2e6d1-134">Note</span><span class="sxs-lookup"><span data-stu-id="2e6d1-134">NOTES</span></span>

## <span data-ttu-id="2e6d1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e6d1-135">RELATED LINKS</span></span>

[<span data-ttu-id="2e6d1-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="2e6d1-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="2e6d1-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
