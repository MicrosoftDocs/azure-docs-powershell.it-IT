---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860246"
---
# <span data-ttu-id="333b9-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="333b9-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="333b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="333b9-102">SYNOPSIS</span></span>
<span data-ttu-id="333b9-103">Opta per la raccolta di dati per migliorare i cmdlet di AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="333b9-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="333b9-104">I dati non vengono raccolti a meno che non si opti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="333b9-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="333b9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="333b9-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333b9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333b9-106">DESCRIPTION</span></span>
<span data-ttu-id="333b9-107">Puoi migliorare l'esperienza dell'uso di Microsoft Cloud ed Azure PowerShell optando per la raccolta di dati.</span><span class="sxs-lookup"><span data-stu-id="333b9-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="333b9-108">In Azure PowerShell non vengono raccolti dati senza il consenso: è necessario esplicitamente eseguire l'opt-in eseguendo Enable-AzDataCollection o rispondendo a Sì quando in Azure PowerShell viene richiesto di raccogliere i dati al primo avvio di un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333b9-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="333b9-109">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e migliorare l'esperienza dell'uso di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="333b9-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="333b9-110">Microsoft Azure PowerShell non raccoglie dati privati o informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="333b9-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="333b9-111">Eseguire il cmdlet Disable-AzDataCollection per disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="333b9-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="333b9-112">In questo modo verrà impedito agli utenti correnti di richiedere la raccolta dei dati per la prima volta che vengono eseguiti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333b9-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="333b9-113">Per abilitare la raccolta dati per l'utente corrente, eseguire il cmdlet Enable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="333b9-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="333b9-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="333b9-114">EXAMPLES</span></span>

### <span data-ttu-id="333b9-115">Esempio 1: disabilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="333b9-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="333b9-116">Questo esempio Mostra come disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="333b9-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="333b9-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="333b9-117">PARAMETERS</span></span>

### <span data-ttu-id="333b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b9-118">-DefaultProfile</span></span>
<span data-ttu-id="333b9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="333b9-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333b9-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="333b9-120">-Confirm</span></span>
<span data-ttu-id="333b9-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333b9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333b9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333b9-122">-WhatIf</span></span>
<span data-ttu-id="333b9-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="333b9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="333b9-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="333b9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b9-125">CommonParameters</span></span>
<span data-ttu-id="333b9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b9-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="333b9-128">INPUTS</span></span>

### <span data-ttu-id="333b9-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="333b9-129">None</span></span>

## <span data-ttu-id="333b9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="333b9-130">OUTPUTS</span></span>

### <span data-ttu-id="333b9-131">System. void</span><span class="sxs-lookup"><span data-stu-id="333b9-131">System.Void</span></span>

## <span data-ttu-id="333b9-132">Note</span><span class="sxs-lookup"><span data-stu-id="333b9-132">NOTES</span></span>

## <span data-ttu-id="333b9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="333b9-133">RELATED LINKS</span></span>

[<span data-ttu-id="333b9-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="333b9-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

