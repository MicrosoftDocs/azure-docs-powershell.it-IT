---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999038"
---
# <span data-ttu-id="14094-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="14094-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="14094-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14094-102">SYNOPSIS</span></span>
<span data-ttu-id="14094-103">Consente ad Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14094-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="14094-104">L'esecuzione di questo cmdlet acconsente esplicitamente alla raccolta dei dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="14094-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="14094-105">I dati vengono raccolti per impostazione predefinita, a meno che tu non lo rifiuti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="14094-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="14094-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14094-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14094-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14094-107">DESCRIPTION</span></span>

<span data-ttu-id="14094-108">Il `Enable-AzDataCollection` cmdlet viene usato per acconsentire esplicitamente alla raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="14094-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="14094-109">Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="14094-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="14094-110">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, identificare i problemi comuni e migliorare l'esperienza di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14094-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="14094-111">Microsoft Azure PowerShell non raccoglie dati privati o personali.</span><span class="sxs-lookup"><span data-stu-id="14094-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="14094-112">Per disabilitare la raccolta dei dati, è necessario rifiutare esplicitamente eseguendo `Disable-AzDataCollection` l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="14094-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="14094-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14094-113">EXAMPLES</span></span>

### <span data-ttu-id="14094-114">Esempio 1: Abilitazione della raccolta dei dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="14094-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="14094-115">L'esempio seguente mostra come abilitare la raccolta dei dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="14094-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="14094-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14094-116">PARAMETERS</span></span>

### <span data-ttu-id="14094-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14094-117">-DefaultProfile</span></span>

<span data-ttu-id="14094-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14094-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14094-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14094-119">-Confirm</span></span>

<span data-ttu-id="14094-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14094-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14094-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14094-121">-WhatIf</span></span>

<span data-ttu-id="14094-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14094-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14094-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14094-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14094-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14094-124">CommonParameters</span></span>
<span data-ttu-id="14094-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14094-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14094-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14094-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14094-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="14094-127">INPUTS</span></span>

### <span data-ttu-id="14094-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14094-128">None</span></span>

## <span data-ttu-id="14094-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14094-129">OUTPUTS</span></span>

### <span data-ttu-id="14094-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="14094-130">System.Void</span></span>

## <span data-ttu-id="14094-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="14094-131">NOTES</span></span>

## <span data-ttu-id="14094-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14094-132">RELATED LINKS</span></span>

[<span data-ttu-id="14094-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="14094-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
