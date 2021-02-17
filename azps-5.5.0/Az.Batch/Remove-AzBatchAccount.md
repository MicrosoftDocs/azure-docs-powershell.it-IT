---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205195"
---
# <span data-ttu-id="03779-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="03779-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="03779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03779-102">SYNOPSIS</span></span>
<span data-ttu-id="03779-103">Rimuove un account batch.</span><span class="sxs-lookup"><span data-stu-id="03779-103">Removes a Batch account.</span></span>

## <span data-ttu-id="03779-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03779-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03779-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03779-105">DESCRIPTION</span></span>
<span data-ttu-id="03779-106">Il cmdlet **Remove-AzBatchAccount** rimuove un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="03779-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="03779-107">Questo cmdlet chiede di confermare la rimozione di un account, a meno che non si specifica *il parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="03779-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="03779-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03779-108">EXAMPLES</span></span>

### <span data-ttu-id="03779-109">Esempio 1: Rimuovere un account batch</span><span class="sxs-lookup"><span data-stu-id="03779-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="03779-110">Questo comando rimuove l'account batch denominato pio.</span><span class="sxs-lookup"><span data-stu-id="03779-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="03779-111">Questo comando richiede conferma prima di eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="03779-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="03779-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03779-112">PARAMETERS</span></span>

### <span data-ttu-id="03779-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03779-113">-AccountName</span></span>
<span data-ttu-id="03779-114">Specifica il nome dell'account batch rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03779-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03779-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03779-115">-DefaultProfile</span></span>
<span data-ttu-id="03779-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03779-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03779-117">-Force</span><span class="sxs-lookup"><span data-stu-id="03779-117">-Force</span></span>
<span data-ttu-id="03779-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="03779-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03779-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03779-119">-ResourceGroupName</span></span>
<span data-ttu-id="03779-120">Specifica il gruppo di risorse dell'account rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03779-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03779-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03779-121">-Confirm</span></span>
<span data-ttu-id="03779-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03779-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03779-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03779-123">-WhatIf</span></span>
<span data-ttu-id="03779-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03779-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03779-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03779-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03779-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03779-126">CommonParameters</span></span>
<span data-ttu-id="03779-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03779-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03779-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03779-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03779-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="03779-129">INPUTS</span></span>

### <span data-ttu-id="03779-130">System.String</span><span class="sxs-lookup"><span data-stu-id="03779-130">System.String</span></span>

## <span data-ttu-id="03779-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03779-131">OUTPUTS</span></span>

### <span data-ttu-id="03779-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="03779-132">System.Void</span></span>

## <span data-ttu-id="03779-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="03779-133">NOTES</span></span>

## <span data-ttu-id="03779-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03779-134">RELATED LINKS</span></span>

[<span data-ttu-id="03779-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="03779-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="03779-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="03779-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="03779-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="03779-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="03779-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="03779-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
