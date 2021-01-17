---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475677"
---
# <span data-ttu-id="5884a-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="5884a-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="5884a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5884a-102">SYNOPSIS</span></span>
<span data-ttu-id="5884a-103">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="5884a-103">Check the availability of a name.</span></span> <span data-ttu-id="5884a-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="5884a-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="5884a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5884a-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5884a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5884a-106">DESCRIPTION</span></span>
<span data-ttu-id="5884a-107">Verificare la disponibilità di un nome.</span><span class="sxs-lookup"><span data-stu-id="5884a-107">Check the availability of a name.</span></span> <span data-ttu-id="5884a-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="5884a-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="5884a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5884a-109">EXAMPLES</span></span>

### <span data-ttu-id="5884a-110">Controllare un nome esistente.</span><span class="sxs-lookup"><span data-stu-id="5884a-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="5884a-111">Selezionare un nome inesistente.</span><span class="sxs-lookup"><span data-stu-id="5884a-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="5884a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5884a-112">PARAMETERS</span></span>

### <span data-ttu-id="5884a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5884a-113">-DefaultProfile</span></span>
<span data-ttu-id="5884a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5884a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5884a-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5884a-115">-Location</span></span>
<span data-ttu-id="5884a-116">Posizione del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="5884a-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="5884a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5884a-117">-Name</span></span>
<span data-ttu-id="5884a-118">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="5884a-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="5884a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5884a-119">CommonParameters</span></span>
<span data-ttu-id="5884a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5884a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5884a-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5884a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5884a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5884a-122">INPUTS</span></span>

### <span data-ttu-id="5884a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5884a-123">System.String</span></span>

## <span data-ttu-id="5884a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5884a-124">OUTPUTS</span></span>

### <span data-ttu-id="5884a-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5884a-125">System.Boolean</span></span>

## <span data-ttu-id="5884a-126">Note</span><span class="sxs-lookup"><span data-stu-id="5884a-126">NOTES</span></span>

## <span data-ttu-id="5884a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5884a-127">RELATED LINKS</span></span>
