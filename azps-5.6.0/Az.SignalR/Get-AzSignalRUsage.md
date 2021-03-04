---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955486"
---
# <span data-ttu-id="3b19f-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="3b19f-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="3b19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b19f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b19f-103">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3b19f-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="3b19f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b19f-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b19f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b19f-105">DESCRIPTION</span></span>
<span data-ttu-id="3b19f-106">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3b19f-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="3b19f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b19f-107">EXAMPLES</span></span>

### <span data-ttu-id="3b19f-108">Ottenere la quota di utilizzo immessa la posizione</span><span class="sxs-lookup"><span data-stu-id="3b19f-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="3b19f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b19f-109">PARAMETERS</span></span>

### <span data-ttu-id="3b19f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b19f-110">-DefaultProfile</span></span>
<span data-ttu-id="3b19f-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b19f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b19f-112">-Location</span><span class="sxs-lookup"><span data-stu-id="3b19f-112">-Location</span></span>
<span data-ttu-id="3b19f-113">Posizione del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="3b19f-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b19f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b19f-114">CommonParameters</span></span>
<span data-ttu-id="3b19f-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b19f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b19f-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b19f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b19f-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b19f-117">INPUTS</span></span>

### <span data-ttu-id="3b19f-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3b19f-118">None</span></span>

## <span data-ttu-id="3b19f-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b19f-119">OUTPUTS</span></span>

### <span data-ttu-id="3b19f-120">Microsoft.Azure.Commands.Signalr.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="3b19f-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="3b19f-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b19f-121">NOTES</span></span>

## <span data-ttu-id="3b19f-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b19f-122">RELATED LINKS</span></span>
