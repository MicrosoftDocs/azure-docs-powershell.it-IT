---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193938"
---
# <span data-ttu-id="edc18-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="edc18-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="edc18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edc18-102">SYNOPSIS</span></span>
<span data-ttu-id="edc18-103">Ottenere o elencare le SKU di Virtual Appliance di rete disponibili nell'inventario.</span><span class="sxs-lookup"><span data-stu-id="edc18-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="edc18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edc18-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edc18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edc18-105">DESCRIPTION</span></span>
<span data-ttu-id="edc18-106">L'Get-AzNetworkVirtualApplianceSku Ottiene o elenca le SKU di Virtual Appliance di rete disponibili nell'inventario di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="edc18-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="edc18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edc18-107">EXAMPLES</span></span>

### <span data-ttu-id="edc18-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edc18-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="edc18-109">Ottenere un SKU per nome.</span><span class="sxs-lookup"><span data-stu-id="edc18-109">Get a sku by name.</span></span>

### <span data-ttu-id="edc18-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="edc18-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="edc18-111">Elenca tutti gli SKU disponibili di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="edc18-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="edc18-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edc18-112">PARAMETERS</span></span>

### <span data-ttu-id="edc18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc18-113">-DefaultProfile</span></span>
<span data-ttu-id="edc18-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edc18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc18-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="edc18-115">-SkuName</span></span>
<span data-ttu-id="edc18-116">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="edc18-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc18-117">CommonParameters</span></span>
<span data-ttu-id="edc18-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc18-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edc18-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc18-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edc18-120">INPUTS</span></span>

### <span data-ttu-id="edc18-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="edc18-121">None</span></span>

## <span data-ttu-id="edc18-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edc18-122">OUTPUTS</span></span>

### <span data-ttu-id="edc18-123">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="edc18-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="edc18-124">Note</span><span class="sxs-lookup"><span data-stu-id="edc18-124">NOTES</span></span>

## <span data-ttu-id="edc18-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edc18-125">RELATED LINKS</span></span>