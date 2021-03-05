---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 5b74f378bc867c1d39f27ebdd9972dfdda5457c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007326"
---
# <span data-ttu-id="8db8c-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8db8c-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="8db8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db8c-102">SYNOPSIS</span></span>
<span data-ttu-id="8db8c-103">Rimuove un account batch.</span><span class="sxs-lookup"><span data-stu-id="8db8c-103">Removes a Batch account.</span></span>

## <span data-ttu-id="8db8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8db8c-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db8c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8db8c-105">DESCRIPTION</span></span>
<span data-ttu-id="8db8c-106">Il cmdlet **Remove-AzBatchAccount** rimuove un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="8db8c-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="8db8c-107">Questo cmdlet chiede di confermare la rimozione di un account, a meno che non si specifica *il parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="8db8c-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="8db8c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8db8c-108">EXAMPLES</span></span>

### <span data-ttu-id="8db8c-109">Esempio 1: Rimuovere un account batch</span><span class="sxs-lookup"><span data-stu-id="8db8c-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="8db8c-110">Questo comando rimuove l'account batch denominato pio.</span><span class="sxs-lookup"><span data-stu-id="8db8c-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="8db8c-111">Questo comando richiede conferma prima di eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="8db8c-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="8db8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8db8c-112">PARAMETERS</span></span>

### <span data-ttu-id="8db8c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8db8c-113">-AccountName</span></span>
<span data-ttu-id="8db8c-114">Specifica il nome dell'account batch rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db8c-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db8c-115">-DefaultProfile</span></span>
<span data-ttu-id="8db8c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8db8c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db8c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8db8c-117">-Force</span></span>
<span data-ttu-id="8db8c-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8db8c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db8c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db8c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8db8c-120">Specifica il gruppo di risorse dell'account rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db8c-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db8c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8db8c-121">-Confirm</span></span>
<span data-ttu-id="8db8c-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db8c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db8c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db8c-123">-WhatIf</span></span>
<span data-ttu-id="8db8c-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8db8c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8db8c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8db8c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db8c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db8c-126">CommonParameters</span></span>
<span data-ttu-id="8db8c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db8c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db8c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8db8c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db8c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8db8c-129">INPUTS</span></span>

### <span data-ttu-id="8db8c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8db8c-130">System.String</span></span>

## <span data-ttu-id="8db8c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8db8c-131">OUTPUTS</span></span>

### <span data-ttu-id="8db8c-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="8db8c-132">System.Void</span></span>

## <span data-ttu-id="8db8c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8db8c-133">NOTES</span></span>

## <span data-ttu-id="8db8c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8db8c-134">RELATED LINKS</span></span>

[<span data-ttu-id="8db8c-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8db8c-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="8db8c-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8db8c-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="8db8c-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8db8c-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="8db8c-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="8db8c-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
