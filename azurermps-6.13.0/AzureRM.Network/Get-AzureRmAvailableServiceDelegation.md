---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686906"
---
# <span data-ttu-id="0661f-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="0661f-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="0661f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0661f-102">SYNOPSIS</span></span>
<span data-ttu-id="0661f-103">Ottenere le delegazioni dei servizi disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="0661f-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0661f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0661f-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0661f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0661f-105">DESCRIPTION</span></span>
<span data-ttu-id="0661f-106">Il cmdlet **Get-AzureRmAvailableServiceDelegation** consente di recuperare tutte le delegazioni di servizi disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="0661f-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="0661f-107">Questo cmdlet *non* descrive le delegazioni che possono coesistere in una singola subnet.</span><span class="sxs-lookup"><span data-stu-id="0661f-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="0661f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0661f-108">EXAMPLES</span></span>

### <span data-ttu-id="0661f-109">1: ottenere tutte le delegazioni di servizi disponibili</span><span class="sxs-lookup"><span data-stu-id="0661f-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="0661f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0661f-110">PARAMETERS</span></span>

### <span data-ttu-id="0661f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0661f-111">-DefaultProfile</span></span>
<span data-ttu-id="0661f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0661f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0661f-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0661f-113">-Location</span></span>
<span data-ttu-id="0661f-114">La posizione.</span><span class="sxs-lookup"><span data-stu-id="0661f-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0661f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0661f-115">CommonParameters</span></span>
<span data-ttu-id="0661f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0661f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0661f-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0661f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0661f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0661f-118">INPUTS</span></span>

### <span data-ttu-id="0661f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0661f-119">System.String</span></span>

## <span data-ttu-id="0661f-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0661f-120">OUTPUTS</span></span>

### <span data-ttu-id="0661f-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="0661f-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="0661f-122">Note</span><span class="sxs-lookup"><span data-stu-id="0661f-122">NOTES</span></span>

## <span data-ttu-id="0661f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0661f-123">RELATED LINKS</span></span>
<span data-ttu-id="0661f-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="0661f-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
