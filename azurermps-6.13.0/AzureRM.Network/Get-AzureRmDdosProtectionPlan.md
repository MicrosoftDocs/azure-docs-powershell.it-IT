---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686905"
---
# <span data-ttu-id="061af-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="061af-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="061af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="061af-102">SYNOPSIS</span></span>
<span data-ttu-id="061af-103">Ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="061af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="061af-104">SYNTAX</span></span>

### <span data-ttu-id="061af-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="061af-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="061af-106">Elenco</span><span class="sxs-lookup"><span data-stu-id="061af-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="061af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="061af-107">DESCRIPTION</span></span>
<span data-ttu-id="061af-108">Il cmdlet Get-AzureRmDdosProtectionPlan ottiene un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="061af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="061af-109">EXAMPLES</span></span>

### <span data-ttu-id="061af-110">Esempio 1: ottenere un piano di protezione DDoS specifico</span><span class="sxs-lookup"><span data-stu-id="061af-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="061af-111">In questo caso, è necessario specificare sia gli attributi **ResourceGroupName** che i **nomi** , che corrispondono rispettivamente al gruppo di risorse e al nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="061af-112">Esempio 2: ottenere tutti i piani di protezione DDoS in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="061af-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="061af-113">In questo scenario specifichiamo solo il parametro **ResourceGroupName** per ottenere un elenco dei piani di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="061af-114">Esempio 2: ottenere tutti i piani di protezione DDoS in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="061af-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="061af-115">In questo caso, non specifichiamo alcun parametro per ottenere un elenco di tutti i piani di protezione DDoS in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="061af-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="061af-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="061af-116">PARAMETERS</span></span>

### <span data-ttu-id="061af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061af-117">-DefaultProfile</span></span>
<span data-ttu-id="061af-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="061af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="061af-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="061af-119">-Name</span></span>
<span data-ttu-id="061af-120">Specifica il nome del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="061af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061af-121">-ResourceGroupName</span></span>
<span data-ttu-id="061af-122">Specifica il nome del gruppo di risorse del piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="061af-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="061af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061af-123">CommonParameters</span></span>
<span data-ttu-id="061af-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061af-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="061af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061af-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="061af-126">INPUTS</span></span>

### <span data-ttu-id="061af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="061af-127">System.String</span></span>

## <span data-ttu-id="061af-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="061af-128">OUTPUTS</span></span>

### <span data-ttu-id="061af-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="061af-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="061af-130">Note</span><span class="sxs-lookup"><span data-stu-id="061af-130">NOTES</span></span>

## <span data-ttu-id="061af-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="061af-131">RELATED LINKS</span></span>

[<span data-ttu-id="061af-132">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="061af-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="061af-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="061af-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="061af-134">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="061af-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="061af-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="061af-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="061af-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="061af-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
