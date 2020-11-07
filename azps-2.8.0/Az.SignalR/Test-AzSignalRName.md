---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 21fbee422b898b5e5cf448f4a8f1913777268964
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854513"
---
# <span data-ttu-id="2b944-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="2b944-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="2b944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b944-102">SYNOPSIS</span></span>
<span data-ttu-id="2b944-103">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="2b944-103">Check the availability of a name.</span></span> <span data-ttu-id="2b944-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="2b944-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="2b944-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b944-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b944-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b944-106">DESCRIPTION</span></span>
<span data-ttu-id="2b944-107">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="2b944-107">Check the availability of a name.</span></span> <span data-ttu-id="2b944-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="2b944-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="2b944-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b944-109">EXAMPLES</span></span>

### <span data-ttu-id="2b944-110">Controllare un nome esistente.</span><span class="sxs-lookup"><span data-stu-id="2b944-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="2b944-111">Selezionare un nome inesistente.</span><span class="sxs-lookup"><span data-stu-id="2b944-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="2b944-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b944-112">PARAMETERS</span></span>

### <span data-ttu-id="2b944-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b944-113">-DefaultProfile</span></span>
<span data-ttu-id="2b944-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b944-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b944-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2b944-115">-Location</span></span>
<span data-ttu-id="2b944-116">Posizione del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="2b944-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="2b944-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b944-117">-Name</span></span>
<span data-ttu-id="2b944-118">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="2b944-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="2b944-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b944-119">CommonParameters</span></span>
<span data-ttu-id="2b944-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b944-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b944-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b944-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b944-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b944-122">INPUTS</span></span>

### <span data-ttu-id="2b944-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2b944-123">System.String</span></span>

## <span data-ttu-id="2b944-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b944-124">OUTPUTS</span></span>

### <span data-ttu-id="2b944-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b944-125">System.Boolean</span></span>

## <span data-ttu-id="2b944-126">Note</span><span class="sxs-lookup"><span data-stu-id="2b944-126">NOTES</span></span>

## <span data-ttu-id="2b944-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b944-127">RELATED LINKS</span></span>
