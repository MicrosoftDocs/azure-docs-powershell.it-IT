---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 2b5cc008e96d12828d5f834fd5fa4a30f83ea70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967950"
---
# <span data-ttu-id="20989-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="20989-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="20989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20989-102">SYNOPSIS</span></span>
<span data-ttu-id="20989-103">Ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="20989-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20989-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20989-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20989-105">DESCRIPTION</span></span>
<span data-ttu-id="20989-106">Il cmdlet Get-AzDdosProtectionPlan cmdlet ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="20989-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20989-107">EXAMPLES</span></span>

### <span data-ttu-id="20989-108">Esempio 1: Ottenere un piano di protezione DDoS specifico</span><span class="sxs-lookup"><span data-stu-id="20989-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="20989-109">In questo caso, è necessario specificare gli attributi **ResourceGroupName** e **Name,** che corrispondono rispettivamente al gruppo di risorse e al nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="20989-110">Esempio 2: Ottenere tutti i piani di protezione DDoS in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="20989-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="20989-111">In questo scenario viene specificato solo il parametro **ResourceGroupName** per ottenere un elenco di piani di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="20989-112">Esempio 3: Ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="20989-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="20989-113">Qui non viene specificato alcun parametro per ottenere un elenco di tutti i piani di protezione DDoS in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="20989-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="20989-114">Esempio 4: Ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="20989-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="20989-115">Questo cmdlet restituisce tutti gli elementi DdosProtectionPlan che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="20989-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="20989-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20989-116">PARAMETERS</span></span>

### <span data-ttu-id="20989-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20989-117">-DefaultProfile</span></span>
<span data-ttu-id="20989-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20989-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20989-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20989-119">-Name</span></span>
<span data-ttu-id="20989-120">Specifica il nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="20989-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20989-121">-ResourceGroupName</span></span>
<span data-ttu-id="20989-122">Specifica il nome del gruppo di risorse del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="20989-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="20989-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20989-123">CommonParameters</span></span>
<span data-ttu-id="20989-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20989-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20989-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20989-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20989-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="20989-126">INPUTS</span></span>

### <span data-ttu-id="20989-127">System.String</span><span class="sxs-lookup"><span data-stu-id="20989-127">System.String</span></span>

## <span data-ttu-id="20989-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20989-128">OUTPUTS</span></span>

### <span data-ttu-id="20989-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="20989-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="20989-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="20989-130">NOTES</span></span>

## <span data-ttu-id="20989-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20989-131">RELATED LINKS</span></span>

[<span data-ttu-id="20989-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="20989-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="20989-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="20989-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="20989-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20989-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="20989-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20989-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="20989-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20989-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)