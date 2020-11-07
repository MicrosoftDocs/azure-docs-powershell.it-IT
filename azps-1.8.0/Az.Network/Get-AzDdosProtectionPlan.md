---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 729f89742c7dd3249124f2d2404ab85f08db0e86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678574"
---
# <span data-ttu-id="a9f50-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="a9f50-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="a9f50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9f50-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f50-103">Ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="a9f50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9f50-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f50-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9f50-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f50-106">Il cmdlet Get-AzDdosProtectionPlan ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="a9f50-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9f50-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f50-108">Esempio 1: ottenere un piano di protezione DDoS specifico</span><span class="sxs-lookup"><span data-stu-id="a9f50-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="a9f50-109">In questo caso, è necessario specificare sia gli attributi **ResourceGroupName** che i **nomi** , che corrispondono rispettivamente al gruppo di risorse e al nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="a9f50-110">Esempio 2: ottenere tutti i piani di protezione DDoS in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a9f50-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="a9f50-111">In questo scenario specifichiamo solo il parametro **ResourceGroupName** per ottenere un elenco dei piani di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="a9f50-112">Esempio 3: ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a9f50-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="a9f50-113">In questo caso, non specifichiamo alcun parametro per ottenere un elenco di tutti i piani di protezione DDoS in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a9f50-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="a9f50-114">Esempio 4: ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a9f50-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="a9f50-115">Questo cmdlet restituisce tutti i DdosProtectionPlans che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="a9f50-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="a9f50-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9f50-116">PARAMETERS</span></span>

### <span data-ttu-id="a9f50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f50-117">-DefaultProfile</span></span>
<span data-ttu-id="a9f50-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f50-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9f50-119">-Name</span></span>
<span data-ttu-id="a9f50-120">Specifica il nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="a9f50-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f50-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9f50-122">Specifica il nome del gruppo di risorse del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="a9f50-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="a9f50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f50-123">CommonParameters</span></span>
<span data-ttu-id="a9f50-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f50-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9f50-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f50-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9f50-126">INPUTS</span></span>

### <span data-ttu-id="a9f50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f50-127">System.String</span></span>

## <span data-ttu-id="a9f50-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9f50-128">OUTPUTS</span></span>

### <span data-ttu-id="a9f50-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="a9f50-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="a9f50-130">Note</span><span class="sxs-lookup"><span data-stu-id="a9f50-130">NOTES</span></span>

## <span data-ttu-id="a9f50-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9f50-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9f50-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="a9f50-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="a9f50-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="a9f50-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="a9f50-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9f50-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="a9f50-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9f50-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="a9f50-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9f50-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)