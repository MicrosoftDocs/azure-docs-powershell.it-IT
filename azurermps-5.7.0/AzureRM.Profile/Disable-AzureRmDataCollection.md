---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520435"
---
# <span data-ttu-id="59bf2-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="59bf2-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="59bf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="59bf2-103">Opta per la raccolta di dati per migliorare i cmdlet di AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="59bf2-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="59bf2-104">I dati non vengono raccolti a meno che non si opti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="59bf2-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bf2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59bf2-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59bf2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59bf2-106">DESCRIPTION</span></span>
<span data-ttu-id="59bf2-107">Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.</span><span class="sxs-lookup"><span data-stu-id="59bf2-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="59bf2-108">In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzureRmDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bf2-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="59bf2-109">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="59bf2-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="59bf2-110">Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="59bf2-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="59bf2-111">Eseguire il cmdlet Disable-AzureRMDataCollection per disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="59bf2-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="59bf2-112">In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bf2-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="59bf2-113">Per abilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="59bf2-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="59bf2-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59bf2-114">EXAMPLES</span></span>

### <span data-ttu-id="59bf2-115">Esempio 1: disabilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="59bf2-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="59bf2-116">Questo esempio Mostra come disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="59bf2-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="59bf2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59bf2-117">PARAMETERS</span></span>

### <span data-ttu-id="59bf2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bf2-118">-DefaultProfile</span></span>
<span data-ttu-id="59bf2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59bf2-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59bf2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59bf2-120">-Confirm</span></span>
<span data-ttu-id="59bf2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bf2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59bf2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59bf2-122">-WhatIf</span></span>
<span data-ttu-id="59bf2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59bf2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59bf2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59bf2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59bf2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bf2-125">CommonParameters</span></span>
<span data-ttu-id="59bf2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bf2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bf2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bf2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bf2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59bf2-128">INPUTS</span></span>

### <span data-ttu-id="59bf2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="59bf2-129">None</span></span>
<span data-ttu-id="59bf2-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="59bf2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59bf2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59bf2-131">OUTPUTS</span></span>

### <span data-ttu-id="59bf2-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="59bf2-132">None</span></span>

## <span data-ttu-id="59bf2-133">Note</span><span class="sxs-lookup"><span data-stu-id="59bf2-133">NOTES</span></span>

## <span data-ttu-id="59bf2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59bf2-134">RELATED LINKS</span></span>

[<span data-ttu-id="59bf2-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="59bf2-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

