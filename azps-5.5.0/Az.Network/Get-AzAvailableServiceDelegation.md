---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206963"
---
# <span data-ttu-id="41b4d-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="41b4d-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="41b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="41b4d-103">Ottenere le delegazioni dei servizi disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="41b4d-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="41b4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41b4d-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41b4d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="41b4d-106">Il cmdlet **Get-AzAvailableServiceDelegation** consente di recuperare tutte le delegazioni del servizio disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="41b4d-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="41b4d-107">Questo cmdlet non *descrive* le delegazioni che possono coesistere in una singola subnet.</span><span class="sxs-lookup"><span data-stu-id="41b4d-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="41b4d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41b4d-108">EXAMPLES</span></span>

### <span data-ttu-id="41b4d-109">1: Ottenere tutte le delegazioni dei servizi disponibili</span><span class="sxs-lookup"><span data-stu-id="41b4d-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="41b4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="41b4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b4d-111">-DefaultProfile</span></span>
<span data-ttu-id="41b4d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41b4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b4d-113">-Location</span><span class="sxs-lookup"><span data-stu-id="41b4d-113">-Location</span></span>
<span data-ttu-id="41b4d-114">Posizione.</span><span class="sxs-lookup"><span data-stu-id="41b4d-114">The location.</span></span>

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

### <span data-ttu-id="41b4d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b4d-115">CommonParameters</span></span>
<span data-ttu-id="41b4d-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b4d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b4d-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41b4d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b4d-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="41b4d-118">INPUTS</span></span>

### <span data-ttu-id="41b4d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="41b4d-119">System.String</span></span>

## <span data-ttu-id="41b4d-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41b4d-120">OUTPUTS</span></span>

### <span data-ttu-id="41b4d-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="41b4d-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="41b4d-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="41b4d-122">NOTES</span></span>

## <span data-ttu-id="41b4d-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41b4d-123">RELATED LINKS</span></span>

<span data-ttu-id="41b4d-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="41b4d-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>