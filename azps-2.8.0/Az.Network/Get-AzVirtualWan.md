---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: 107f2b7b41143c2f121b358eaf29c99537f51a69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853621"
---
# <span data-ttu-id="82038-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82038-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="82038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82038-102">SYNOPSIS</span></span>
<span data-ttu-id="82038-103">Ottiene una WAN virtuale o tutte le WAN virtuali in un gruppo o un abbonamento a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="82038-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="82038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82038-104">SYNTAX</span></span>

### <span data-ttu-id="82038-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82038-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82038-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82038-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82038-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82038-107">DESCRIPTION</span></span>
<span data-ttu-id="82038-108">Ottiene una WAN virtuale o tutte le WAN virtuali in un gruppo o un abbonamento a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="82038-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="82038-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82038-109">EXAMPLES</span></span>

### <span data-ttu-id="82038-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82038-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="82038-111">Questo comando consente di ottenere la WAN virtuale denominata myVirtualWAN nel gruppo di risorse testRG.</span><span class="sxs-lookup"><span data-stu-id="82038-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="82038-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="82038-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="82038-113">Questo comando consente di ottenere tutte le WAN virtuali che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="82038-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="82038-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82038-114">PARAMETERS</span></span>

### <span data-ttu-id="82038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82038-115">-DefaultProfile</span></span>
<span data-ttu-id="82038-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82038-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82038-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="82038-117">-Name</span></span>
<span data-ttu-id="82038-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82038-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="82038-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82038-119">-ResourceGroupName</span></span>
<span data-ttu-id="82038-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82038-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="82038-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82038-121">CommonParameters</span></span>
<span data-ttu-id="82038-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82038-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82038-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82038-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82038-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82038-124">INPUTS</span></span>

### <span data-ttu-id="82038-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82038-125">None</span></span>

## <span data-ttu-id="82038-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82038-126">OUTPUTS</span></span>

### <span data-ttu-id="82038-127">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82038-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="82038-128">Note</span><span class="sxs-lookup"><span data-stu-id="82038-128">NOTES</span></span>

## <span data-ttu-id="82038-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82038-129">RELATED LINKS</span></span>

[<span data-ttu-id="82038-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82038-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="82038-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82038-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="82038-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="82038-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
