---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333211"
---
# <span data-ttu-id="f39b8-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f39b8-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="f39b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f39b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f39b8-103">Consente a Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="f39b8-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f39b8-104">L'esecuzione di questo cmdlet consente di optare per la raccolta di dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="f39b8-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="f39b8-105">I dati vengono raccolti per impostazione predefinita, a meno che non vengano esplicitamente rifiutati.</span><span class="sxs-lookup"><span data-stu-id="f39b8-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="f39b8-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f39b8-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39b8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f39b8-107">DESCRIPTION</span></span>

<span data-ttu-id="f39b8-108">Il `Enable-AzDataCollection` cmdlet viene usato per l'opt-in per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="f39b8-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="f39b8-109">Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f39b8-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="f39b8-110">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, per identificare i problemi comuni e per migliorare l'esperienza di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f39b8-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="f39b8-111">Microsoft Azure PowerShell non raccoglie dati personali o privati.</span><span class="sxs-lookup"><span data-stu-id="f39b8-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="f39b8-112">Per disabilitare la raccolta dati, è necessario disconnettersi esplicitamente eseguendo `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="f39b8-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="f39b8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f39b8-113">EXAMPLES</span></span>

### <span data-ttu-id="f39b8-114">Esempio 1: abilitazione della raccolta dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="f39b8-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="f39b8-115">L'esempio seguente mostra come abilitare la raccolta di dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="f39b8-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="f39b8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f39b8-116">PARAMETERS</span></span>

### <span data-ttu-id="f39b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39b8-117">-DefaultProfile</span></span>

<span data-ttu-id="f39b8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f39b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f39b8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f39b8-119">-Confirm</span></span>

<span data-ttu-id="f39b8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39b8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39b8-121">-WhatIf</span></span>

<span data-ttu-id="f39b8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f39b8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f39b8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f39b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39b8-124">CommonParameters</span></span>

<span data-ttu-id="f39b8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39b8-126">Per altre informazioni, Vedi [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="f39b8-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="f39b8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f39b8-127">INPUTS</span></span>

### <span data-ttu-id="f39b8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f39b8-128">None</span></span>

## <span data-ttu-id="f39b8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f39b8-129">OUTPUTS</span></span>

### <span data-ttu-id="f39b8-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f39b8-130">System.Void</span></span>

## <span data-ttu-id="f39b8-131">Note</span><span class="sxs-lookup"><span data-stu-id="f39b8-131">NOTES</span></span>

## <span data-ttu-id="f39b8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f39b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="f39b8-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f39b8-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
