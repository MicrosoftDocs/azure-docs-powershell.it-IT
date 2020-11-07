---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688401"
---
# <span data-ttu-id="a6162-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6162-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="a6162-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6162-102">SYNOPSIS</span></span>
<span data-ttu-id="a6162-103">Ottiene un Azure VirtualHub per nome e ResourceGroupName o elenca tutti gli hub virtuali per ResourceGroupName/abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a6162-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6162-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6162-104">SYNTAX</span></span>

### <span data-ttu-id="a6162-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6162-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6162-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6162-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6162-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6162-107">DESCRIPTION</span></span>
<span data-ttu-id="a6162-108">Ottiene un Azure VirtualHub per nome e ResourceGroupName o elenca tutti gli hub virtuali per ResourceGroupName/abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a6162-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a6162-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6162-109">EXAMPLES</span></span>

### <span data-ttu-id="a6162-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6162-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a6162-111">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="a6162-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a6162-112">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a6162-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="a6162-113">Ottiene quindi l'hub virtuale usando il relativo ResourceGroupName e il resourceName.</span><span class="sxs-lookup"><span data-stu-id="a6162-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="a6162-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6162-114">PARAMETERS</span></span>

### <span data-ttu-id="a6162-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6162-115">-DefaultProfile</span></span>
<span data-ttu-id="a6162-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6162-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6162-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6162-117">-Name</span></span>
<span data-ttu-id="a6162-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a6162-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6162-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6162-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6162-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6162-120">The resource group name.</span></span>

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

### <span data-ttu-id="a6162-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6162-121">CommonParameters</span></span>
<span data-ttu-id="a6162-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6162-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6162-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6162-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6162-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6162-124">INPUTS</span></span>

### <span data-ttu-id="a6162-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6162-125">None</span></span>

## <span data-ttu-id="a6162-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6162-126">OUTPUTS</span></span>

### <span data-ttu-id="a6162-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a6162-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a6162-128">Note</span><span class="sxs-lookup"><span data-stu-id="a6162-128">NOTES</span></span>

## <span data-ttu-id="a6162-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6162-129">RELATED LINKS</span></span>
