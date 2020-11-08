---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189071"
---
# <span data-ttu-id="945b9-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="945b9-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="945b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="945b9-102">SYNOPSIS</span></span>
<span data-ttu-id="945b9-103">Ottenere le delegazioni dei servizi disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="945b9-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="945b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="945b9-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="945b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="945b9-105">DESCRIPTION</span></span>
<span data-ttu-id="945b9-106">Il cmdlet **Get-AzAvailableServiceDelegation** consente di recuperare tutte le delegazioni di servizi disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="945b9-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="945b9-107">Questo cmdlet *non* descrive le delegazioni che possono coesistere in una singola subnet.</span><span class="sxs-lookup"><span data-stu-id="945b9-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="945b9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="945b9-108">EXAMPLES</span></span>

### <span data-ttu-id="945b9-109">1: ottenere tutte le delegazioni di servizi disponibili</span><span class="sxs-lookup"><span data-stu-id="945b9-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="945b9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="945b9-110">PARAMETERS</span></span>

### <span data-ttu-id="945b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945b9-111">-DefaultProfile</span></span>
<span data-ttu-id="945b9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="945b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="945b9-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="945b9-113">-Location</span></span>
<span data-ttu-id="945b9-114">La posizione.</span><span class="sxs-lookup"><span data-stu-id="945b9-114">The location.</span></span>

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

### <span data-ttu-id="945b9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945b9-115">CommonParameters</span></span>
<span data-ttu-id="945b9-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945b9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945b9-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="945b9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945b9-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="945b9-118">INPUTS</span></span>

### <span data-ttu-id="945b9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="945b9-119">System.String</span></span>

## <span data-ttu-id="945b9-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="945b9-120">OUTPUTS</span></span>

### <span data-ttu-id="945b9-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="945b9-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="945b9-122">Note</span><span class="sxs-lookup"><span data-stu-id="945b9-122">NOTES</span></span>

## <span data-ttu-id="945b9-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="945b9-123">RELATED LINKS</span></span>

<span data-ttu-id="945b9-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="945b9-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>