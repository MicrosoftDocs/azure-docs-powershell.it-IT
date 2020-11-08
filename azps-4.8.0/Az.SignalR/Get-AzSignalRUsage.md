---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031048"
---
# <span data-ttu-id="621ea-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="621ea-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="621ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="621ea-102">SYNOPSIS</span></span>
<span data-ttu-id="621ea-103">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="621ea-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="621ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="621ea-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="621ea-105">DESCRIPTION</span></span>
<span data-ttu-id="621ea-106">Ottenere la quota di utilizzo di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="621ea-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="621ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="621ea-107">EXAMPLES</span></span>

### <span data-ttu-id="621ea-108">Ottenere la quota di utilizzo immettendo la posizione</span><span class="sxs-lookup"><span data-stu-id="621ea-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="621ea-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="621ea-109">PARAMETERS</span></span>

### <span data-ttu-id="621ea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621ea-110">-DefaultProfile</span></span>
<span data-ttu-id="621ea-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="621ea-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="621ea-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="621ea-112">-Location</span></span>
<span data-ttu-id="621ea-113">Posizione del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="621ea-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="621ea-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621ea-114">CommonParameters</span></span>
<span data-ttu-id="621ea-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621ea-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621ea-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="621ea-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621ea-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="621ea-117">INPUTS</span></span>

### <span data-ttu-id="621ea-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="621ea-118">None</span></span>

## <span data-ttu-id="621ea-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="621ea-119">OUTPUTS</span></span>

### <span data-ttu-id="621ea-120">Microsoft. Azure. Commands. SignalR. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="621ea-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="621ea-121">Note</span><span class="sxs-lookup"><span data-stu-id="621ea-121">NOTES</span></span>

## <span data-ttu-id="621ea-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="621ea-122">RELATED LINKS</span></span>
