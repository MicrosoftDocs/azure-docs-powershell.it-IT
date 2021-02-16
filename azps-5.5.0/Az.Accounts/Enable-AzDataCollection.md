---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195438"
---
# <span data-ttu-id="ca465-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ca465-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="ca465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca465-102">SYNOPSIS</span></span>
<span data-ttu-id="ca465-103">Consente ad Azure PowerShell di raccogliere dati per migliorare l'esperienza utente con i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca465-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ca465-104">Eseguendo questo cmdlet si acconsente esplicitamente alla raccolta dei dati per l'utente corrente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="ca465-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="ca465-105">I dati vengono raccolti per impostazione predefinita, a meno che tu non lo rifiuti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="ca465-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="ca465-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca465-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca465-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca465-107">DESCRIPTION</span></span>

<span data-ttu-id="ca465-108">Il `Enable-AzDataCollection` cmdlet viene usato per acconsentire esplicitamente alla raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="ca465-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="ca465-109">Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ca465-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="ca465-110">Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo, identificare i problemi comuni e migliorare l'esperienza di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca465-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="ca465-111">Microsoft Azure PowerShell non raccoglie dati privati o personali.</span><span class="sxs-lookup"><span data-stu-id="ca465-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="ca465-112">Per disabilitare la raccolta dei dati, è necessario rifiutare esplicitamente `Disable-AzDataCollection` l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ca465-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="ca465-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca465-113">EXAMPLES</span></span>

### <span data-ttu-id="ca465-114">Esempio 1: Abilitazione della raccolta dei dati per l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="ca465-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="ca465-115">L'esempio seguente mostra come abilitare la raccolta dei dati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="ca465-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="ca465-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca465-116">PARAMETERS</span></span>

### <span data-ttu-id="ca465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca465-117">-DefaultProfile</span></span>

<span data-ttu-id="ca465-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca465-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca465-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca465-119">-Confirm</span></span>

<span data-ttu-id="ca465-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca465-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca465-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca465-121">-WhatIf</span></span>

<span data-ttu-id="ca465-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca465-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca465-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca465-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca465-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca465-124">CommonParameters</span></span>

<span data-ttu-id="ca465-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca465-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca465-126">Per altre informazioni, [vedere](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca465-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="ca465-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca465-127">INPUTS</span></span>

### <span data-ttu-id="ca465-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ca465-128">None</span></span>

## <span data-ttu-id="ca465-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca465-129">OUTPUTS</span></span>

### <span data-ttu-id="ca465-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="ca465-130">System.Void</span></span>

## <span data-ttu-id="ca465-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca465-131">NOTES</span></span>

## <span data-ttu-id="ca465-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca465-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca465-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ca465-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
