---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864395"
---
# <span data-ttu-id="047c3-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="047c3-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="047c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="047c3-102">SYNOPSIS</span></span>
<span data-ttu-id="047c3-103">Ottenere le delegazioni dei servizi disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="047c3-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="047c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="047c3-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="047c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="047c3-105">DESCRIPTION</span></span>
<span data-ttu-id="047c3-106">Il cmdlet **Get-AzAvailableServiceDelegation** consente di recuperare tutte le delegazioni di servizi disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="047c3-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="047c3-107">Questo cmdlet *non* descrive le delegazioni che possono coesistere in una singola subnet.</span><span class="sxs-lookup"><span data-stu-id="047c3-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="047c3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="047c3-108">EXAMPLES</span></span>

### <span data-ttu-id="047c3-109">1: ottenere tutte le delegazioni di servizi disponibili</span><span class="sxs-lookup"><span data-stu-id="047c3-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="047c3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="047c3-110">PARAMETERS</span></span>

### <span data-ttu-id="047c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047c3-111">-DefaultProfile</span></span>
<span data-ttu-id="047c3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="047c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="047c3-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="047c3-113">-Location</span></span>
<span data-ttu-id="047c3-114">La posizione.</span><span class="sxs-lookup"><span data-stu-id="047c3-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047c3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047c3-115">CommonParameters</span></span>
<span data-ttu-id="047c3-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047c3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047c3-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="047c3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047c3-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="047c3-118">INPUTS</span></span>

### <span data-ttu-id="047c3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="047c3-119">System.String</span></span>

## <span data-ttu-id="047c3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="047c3-120">OUTPUTS</span></span>

### <span data-ttu-id="047c3-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="047c3-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="047c3-122">Note</span><span class="sxs-lookup"><span data-stu-id="047c3-122">NOTES</span></span>

## <span data-ttu-id="047c3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="047c3-123">RELATED LINKS</span></span>

<span data-ttu-id="047c3-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="047c3-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>