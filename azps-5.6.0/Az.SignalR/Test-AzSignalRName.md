---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955358"
---
# <span data-ttu-id="04c44-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="04c44-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="04c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c44-102">SYNOPSIS</span></span>
<span data-ttu-id="04c44-103">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="04c44-103">Check the availability of a name.</span></span> <span data-ttu-id="04c44-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="04c44-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="04c44-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04c44-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04c44-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04c44-106">DESCRIPTION</span></span>
<span data-ttu-id="04c44-107">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="04c44-107">Check the availability of a name.</span></span> <span data-ttu-id="04c44-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="04c44-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="04c44-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04c44-109">EXAMPLES</span></span>

### <span data-ttu-id="04c44-110">Controllare un nome esistente.</span><span class="sxs-lookup"><span data-stu-id="04c44-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="04c44-111">Controllare un nome inesistente.</span><span class="sxs-lookup"><span data-stu-id="04c44-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="04c44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04c44-112">PARAMETERS</span></span>

### <span data-ttu-id="04c44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c44-113">-DefaultProfile</span></span>
<span data-ttu-id="04c44-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04c44-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c44-115">-Location</span><span class="sxs-lookup"><span data-stu-id="04c44-115">-Location</span></span>
<span data-ttu-id="04c44-116">Posizione del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="04c44-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c44-117">-Name</span><span class="sxs-lookup"><span data-stu-id="04c44-117">-Name</span></span>
<span data-ttu-id="04c44-118">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="04c44-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="04c44-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c44-119">CommonParameters</span></span>
<span data-ttu-id="04c44-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c44-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c44-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04c44-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c44-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="04c44-122">INPUTS</span></span>

### <span data-ttu-id="04c44-123">System.String</span><span class="sxs-lookup"><span data-stu-id="04c44-123">System.String</span></span>

## <span data-ttu-id="04c44-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04c44-124">OUTPUTS</span></span>

### <span data-ttu-id="04c44-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04c44-125">System.Boolean</span></span>

## <span data-ttu-id="04c44-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="04c44-126">NOTES</span></span>

## <span data-ttu-id="04c44-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04c44-127">RELATED LINKS</span></span>
