---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022913"
---
# <span data-ttu-id="81f60-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81f60-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="81f60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81f60-102">SYNOPSIS</span></span>
<span data-ttu-id="81f60-103">Ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="81f60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81f60-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f60-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81f60-105">DESCRIPTION</span></span>
<span data-ttu-id="81f60-106">Il cmdlet Get-AzDdosProtectionPlan ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="81f60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81f60-107">EXAMPLES</span></span>

### <span data-ttu-id="81f60-108">Esempio 1: ottenere un piano di protezione DDoS specifico</span><span class="sxs-lookup"><span data-stu-id="81f60-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="81f60-109">In questo caso, è necessario specificare sia gli attributi **ResourceGroupName** che i **nomi** , che corrispondono rispettivamente al gruppo di risorse e al nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="81f60-110">Esempio 2: ottenere tutti i piani di protezione DDoS in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="81f60-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="81f60-111">In questo scenario specifichiamo solo il parametro **ResourceGroupName** per ottenere un elenco dei piani di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="81f60-112">Esempio 3: ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="81f60-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="81f60-113">In questo caso, non specifichiamo alcun parametro per ottenere un elenco di tutti i piani di protezione DDoS in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="81f60-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="81f60-114">Esempio 4: ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="81f60-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="81f60-115">Questo cmdlet restituisce tutti i DdosProtectionPlans che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="81f60-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="81f60-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81f60-116">PARAMETERS</span></span>

### <span data-ttu-id="81f60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f60-117">-DefaultProfile</span></span>
<span data-ttu-id="81f60-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81f60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f60-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="81f60-119">-Name</span></span>
<span data-ttu-id="81f60-120">Specifica il nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="81f60-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f60-121">-ResourceGroupName</span></span>
<span data-ttu-id="81f60-122">Specifica il nome del gruppo di risorse del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="81f60-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="81f60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f60-123">CommonParameters</span></span>
<span data-ttu-id="81f60-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f60-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81f60-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f60-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81f60-126">INPUTS</span></span>

### <span data-ttu-id="81f60-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81f60-127">System.String</span></span>

## <span data-ttu-id="81f60-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81f60-128">OUTPUTS</span></span>

### <span data-ttu-id="81f60-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81f60-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="81f60-130">Note</span><span class="sxs-lookup"><span data-stu-id="81f60-130">NOTES</span></span>

## <span data-ttu-id="81f60-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81f60-131">RELATED LINKS</span></span>

[<span data-ttu-id="81f60-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81f60-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="81f60-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81f60-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="81f60-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81f60-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="81f60-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81f60-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="81f60-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81f60-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)