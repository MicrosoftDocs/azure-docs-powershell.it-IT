---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491177"
---
# <span data-ttu-id="eab4e-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="eab4e-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="eab4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eab4e-102">SYNOPSIS</span></span>
<span data-ttu-id="eab4e-103">Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="eab4e-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="eab4e-104">L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="eab4e-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="eab4e-105">Non vengono raccolti dati a meno che non si opti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="eab4e-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="eab4e-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eab4e-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eab4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eab4e-107">DESCRIPTION</span></span>
<span data-ttu-id="eab4e-108">Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.</span><span class="sxs-lookup"><span data-stu-id="eab4e-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="eab4e-109">In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eab4e-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="eab4e-110">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eab4e-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="eab4e-111">Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="eab4e-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="eab4e-112">Eseguire il cmdlet Enable-AzureRMDataCollection per abilitare la raccolta dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="eab4e-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="eab4e-113">In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eab4e-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="eab4e-114">Per disabilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="eab4e-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="eab4e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eab4e-115">EXAMPLES</span></span>

### <span data-ttu-id="eab4e-116">Esempio 1: abilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="eab4e-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="eab4e-117">Questo esempio Mostra come abilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="eab4e-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="eab4e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eab4e-118">PARAMETERS</span></span>

### <span data-ttu-id="eab4e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eab4e-119">-Confirm</span></span>
<span data-ttu-id="eab4e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eab4e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab4e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab4e-121">-WhatIf</span></span>
<span data-ttu-id="eab4e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eab4e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eab4e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eab4e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab4e-124">CommonParameters</span></span>
<span data-ttu-id="eab4e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab4e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab4e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab4e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eab4e-127">INPUTS</span></span>

## <span data-ttu-id="eab4e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eab4e-128">OUTPUTS</span></span>

### <span data-ttu-id="eab4e-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eab4e-129">None</span></span>

## <span data-ttu-id="eab4e-130">Note</span><span class="sxs-lookup"><span data-stu-id="eab4e-130">NOTES</span></span>

## <span data-ttu-id="eab4e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eab4e-131">RELATED LINKS</span></span>

[<span data-ttu-id="eab4e-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="eab4e-132">Disable-AzureRmDataCollection</span></span>]()

