---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686715"
---
# <span data-ttu-id="fd036-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fd036-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="fd036-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd036-102">SYNOPSIS</span></span>
<span data-ttu-id="fd036-103">Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd036-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="fd036-104">L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="fd036-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fd036-105">Non vengono raccolti dati a meno che non si opti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="fd036-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd036-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd036-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd036-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd036-107">DESCRIPTION</span></span>
<span data-ttu-id="fd036-108">Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.</span><span class="sxs-lookup"><span data-stu-id="fd036-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="fd036-109">In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd036-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="fd036-110">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd036-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="fd036-111">Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="fd036-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="fd036-112">Eseguire il cmdlet Enable-AzureRMDataCollection per abilitare la raccolta dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="fd036-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fd036-113">In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd036-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="fd036-114">Per disabilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="fd036-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="fd036-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd036-115">EXAMPLES</span></span>

### <span data-ttu-id="fd036-116">Esempio 1: abilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="fd036-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="fd036-117">Questo esempio Mostra come abilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="fd036-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="fd036-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd036-118">PARAMETERS</span></span>

### <span data-ttu-id="fd036-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd036-119">-DefaultProfile</span></span>
<span data-ttu-id="fd036-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd036-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd036-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd036-121">-Confirm</span></span>
<span data-ttu-id="fd036-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd036-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd036-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd036-123">-WhatIf</span></span>
<span data-ttu-id="fd036-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd036-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd036-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd036-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd036-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd036-126">CommonParameters</span></span>
<span data-ttu-id="fd036-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd036-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd036-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd036-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd036-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd036-129">INPUTS</span></span>

### <span data-ttu-id="fd036-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd036-130">None</span></span>
<span data-ttu-id="fd036-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fd036-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd036-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd036-132">OUTPUTS</span></span>

### <span data-ttu-id="fd036-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd036-133">None</span></span>

## <span data-ttu-id="fd036-134">Note</span><span class="sxs-lookup"><span data-stu-id="fd036-134">NOTES</span></span>

## <span data-ttu-id="fd036-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd036-135">RELATED LINKS</span></span>

[<span data-ttu-id="fd036-136">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fd036-136">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

