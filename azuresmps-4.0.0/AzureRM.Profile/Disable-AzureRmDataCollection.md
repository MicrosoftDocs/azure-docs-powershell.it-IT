---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491181"
---
# <span data-ttu-id="81778-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="81778-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="81778-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81778-102">SYNOPSIS</span></span>
<span data-ttu-id="81778-103">Opta per la raccolta di dati per migliorare i cmdlet di AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="81778-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="81778-104">I dati non vengono raccolti a meno che non si opti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="81778-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="81778-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81778-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81778-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81778-106">DESCRIPTION</span></span>
<span data-ttu-id="81778-107">Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.</span><span class="sxs-lookup"><span data-stu-id="81778-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="81778-108">In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81778-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="81778-109">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81778-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="81778-110">Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="81778-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="81778-111">Eseguire il cmdlet Disable-AzureRMDataCollection per disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="81778-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="81778-112">In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81778-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="81778-113">Per abilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="81778-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="81778-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81778-114">EXAMPLES</span></span>

### <span data-ttu-id="81778-115">Esempio 1: disabilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="81778-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="81778-116">Questo esempio Mostra come disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="81778-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="81778-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81778-117">PARAMETERS</span></span>

### <span data-ttu-id="81778-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81778-118">-Confirm</span></span>
<span data-ttu-id="81778-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81778-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81778-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81778-120">-WhatIf</span></span>
<span data-ttu-id="81778-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81778-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81778-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81778-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81778-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81778-123">CommonParameters</span></span>
<span data-ttu-id="81778-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81778-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81778-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81778-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81778-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81778-126">INPUTS</span></span>

## <span data-ttu-id="81778-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81778-127">OUTPUTS</span></span>

### <span data-ttu-id="81778-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="81778-128">None</span></span>

## <span data-ttu-id="81778-129">Note</span><span class="sxs-lookup"><span data-stu-id="81778-129">NOTES</span></span>

## <span data-ttu-id="81778-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81778-130">RELATED LINKS</span></span>

[<span data-ttu-id="81778-131">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="81778-131">Enable-AzureRmDataCollection</span></span>]()

