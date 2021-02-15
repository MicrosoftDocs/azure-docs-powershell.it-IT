---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189038"
---
# <span data-ttu-id="abdcb-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="abdcb-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="abdcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abdcb-102">SYNOPSIS</span></span>
<span data-ttu-id="abdcb-103">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="abdcb-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="abdcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abdcb-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abdcb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="abdcb-105">DESCRIPTION</span></span>
<span data-ttu-id="abdcb-106">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="abdcb-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="abdcb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abdcb-107">EXAMPLES</span></span>

### <span data-ttu-id="abdcb-108">Ottenere la quota di utilizzo immessa la posizione</span><span class="sxs-lookup"><span data-stu-id="abdcb-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="abdcb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abdcb-109">PARAMETERS</span></span>

### <span data-ttu-id="abdcb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdcb-110">-DefaultProfile</span></span>
<span data-ttu-id="abdcb-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abdcb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abdcb-112">-Location</span><span class="sxs-lookup"><span data-stu-id="abdcb-112">-Location</span></span>
<span data-ttu-id="abdcb-113">Posizione del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="abdcb-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="abdcb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdcb-114">CommonParameters</span></span>
<span data-ttu-id="abdcb-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abdcb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdcb-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="abdcb-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdcb-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="abdcb-117">INPUTS</span></span>

### <span data-ttu-id="abdcb-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="abdcb-118">None</span></span>

## <span data-ttu-id="abdcb-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abdcb-119">OUTPUTS</span></span>

### <span data-ttu-id="abdcb-120">Microsoft.Azure.Commands.Signalr.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="abdcb-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="abdcb-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="abdcb-121">NOTES</span></span>

## <span data-ttu-id="abdcb-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abdcb-122">RELATED LINKS</span></span>
