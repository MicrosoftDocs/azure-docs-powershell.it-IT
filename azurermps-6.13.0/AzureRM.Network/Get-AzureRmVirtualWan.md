---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513744"
---
# <span data-ttu-id="6bc5d-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6bc5d-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="6bc5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6bc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc5d-103">Ottiene una WAN virtuale o tutte le WAN virtuali in un gruppo o un abbonamento a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bc5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6bc5d-104">SYNTAX</span></span>

### <span data-ttu-id="6bc5d-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6bc5d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bc5d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc5d-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bc5d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bc5d-107">DESCRIPTION</span></span>
<span data-ttu-id="6bc5d-108">Ottiene una WAN virtuale o tutte le WAN virtuali in un gruppo o un abbonamento a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="6bc5d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6bc5d-109">EXAMPLES</span></span>

### <span data-ttu-id="6bc5d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6bc5d-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="6bc5d-111">Questo comando consente di ottenere la WAN virtuale denominata myVirtualWAN nel gruppo di risorse testRG.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="6bc5d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6bc5d-112">PARAMETERS</span></span>

### <span data-ttu-id="6bc5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc5d-113">-DefaultProfile</span></span>
<span data-ttu-id="6bc5d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc5d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bc5d-115">-Name</span></span>
<span data-ttu-id="6bc5d-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="6bc5d-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc5d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc5d-119">CommonParameters</span></span>
<span data-ttu-id="6bc5d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc5d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc5d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc5d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc5d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6bc5d-122">INPUTS</span></span>

### <span data-ttu-id="6bc5d-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6bc5d-123">None</span></span>

## <span data-ttu-id="6bc5d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6bc5d-124">OUTPUTS</span></span>

### <span data-ttu-id="6bc5d-125">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6bc5d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="6bc5d-126">Note</span><span class="sxs-lookup"><span data-stu-id="6bc5d-126">NOTES</span></span>

## <span data-ttu-id="6bc5d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6bc5d-127">RELATED LINKS</span></span>
