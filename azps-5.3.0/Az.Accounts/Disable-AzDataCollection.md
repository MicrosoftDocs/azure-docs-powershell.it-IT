---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479192"
---
# <span data-ttu-id="f75cf-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f75cf-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="f75cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f75cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f75cf-103">Opta per la raccolta di dati per migliorare i cmdlet di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="f75cf-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f75cf-104">I dati vengono raccolti per impostazione predefinita, a meno che non vengano esplicitamente rifiutati.</span><span class="sxs-lookup"><span data-stu-id="f75cf-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="f75cf-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f75cf-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f75cf-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f75cf-106">DESCRIPTION</span></span>

<span data-ttu-id="f75cf-107">Il `Disable-AzDataCollection` cmdlet viene usato per rifiutare la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="f75cf-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="f75cf-108">Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f75cf-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="f75cf-109">Per disabilitare la raccolta dati, è necessario escludere esplicitamente l'opzione. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e per migliorare l'esperienza di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f75cf-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="f75cf-110">Microsoft Azure PowerShell non raccoglie dati personali o privati.</span><span class="sxs-lookup"><span data-stu-id="f75cf-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="f75cf-111">Se in precedenza è stato scelto, eseguire il `Enable-AzDataCollection` cmdlet per riattivare la raccolta dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="f75cf-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="f75cf-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f75cf-112">EXAMPLES</span></span>

### <span data-ttu-id="f75cf-113">Esempio 1: disabilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="f75cf-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="f75cf-114">L'esempio seguente mostra come disabilitare la raccolta dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="f75cf-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="f75cf-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f75cf-115">PARAMETERS</span></span>

### <span data-ttu-id="f75cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75cf-116">-DefaultProfile</span></span>

<span data-ttu-id="f75cf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f75cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f75cf-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f75cf-118">-Confirm</span></span>

<span data-ttu-id="f75cf-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75cf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75cf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75cf-120">-WhatIf</span></span>

<span data-ttu-id="f75cf-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f75cf-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f75cf-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f75cf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75cf-123">CommonParameters</span></span>

<span data-ttu-id="f75cf-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75cf-125">Per altre informazioni, Vedi [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="f75cf-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="f75cf-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f75cf-126">INPUTS</span></span>

### <span data-ttu-id="f75cf-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f75cf-127">None</span></span>

## <span data-ttu-id="f75cf-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f75cf-128">OUTPUTS</span></span>

### <span data-ttu-id="f75cf-129">System. void</span><span class="sxs-lookup"><span data-stu-id="f75cf-129">System.Void</span></span>

## <span data-ttu-id="f75cf-130">Note</span><span class="sxs-lookup"><span data-stu-id="f75cf-130">NOTES</span></span>

## <span data-ttu-id="f75cf-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f75cf-131">RELATED LINKS</span></span>

[<span data-ttu-id="f75cf-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f75cf-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
