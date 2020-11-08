---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 2dc76b09a48b3e34f01378405437f39782df56f0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030672"
---
# <span data-ttu-id="e5211-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5211-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="e5211-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5211-102">SYNOPSIS</span></span>
<span data-ttu-id="e5211-103">Rimuove un account batch.</span><span class="sxs-lookup"><span data-stu-id="e5211-103">Removes a Batch account.</span></span>

## <span data-ttu-id="e5211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5211-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5211-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5211-105">DESCRIPTION</span></span>
<span data-ttu-id="e5211-106">Il cmdlet **Remove-AzBatchAccount** rimuove un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5211-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="e5211-107">Questo cmdlet richiede prima che venga rimosso un account, a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="e5211-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="e5211-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5211-108">EXAMPLES</span></span>

### <span data-ttu-id="e5211-109">Esempio 1: rimuovere un account batch</span><span class="sxs-lookup"><span data-stu-id="e5211-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="e5211-110">Questo comando consente di rimuovere l'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="e5211-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="e5211-111">Questo comando richiede conferma prima di eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="e5211-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="e5211-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5211-112">PARAMETERS</span></span>

### <span data-ttu-id="e5211-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e5211-113">-AccountName</span></span>
<span data-ttu-id="e5211-114">Specifica il nome dell'account batch rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5211-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e5211-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5211-115">-DefaultProfile</span></span>
<span data-ttu-id="e5211-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5211-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5211-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e5211-117">-Force</span></span>
<span data-ttu-id="e5211-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e5211-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5211-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5211-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5211-120">Specifica il gruppo di risorse dell'account rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5211-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e5211-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5211-121">-Confirm</span></span>
<span data-ttu-id="e5211-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5211-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5211-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5211-123">-WhatIf</span></span>
<span data-ttu-id="e5211-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5211-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5211-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5211-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5211-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5211-126">CommonParameters</span></span>
<span data-ttu-id="e5211-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5211-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5211-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5211-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5211-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5211-129">INPUTS</span></span>

### <span data-ttu-id="e5211-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e5211-130">System.String</span></span>

## <span data-ttu-id="e5211-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5211-131">OUTPUTS</span></span>

### <span data-ttu-id="e5211-132">System. void</span><span class="sxs-lookup"><span data-stu-id="e5211-132">System.Void</span></span>

## <span data-ttu-id="e5211-133">Note</span><span class="sxs-lookup"><span data-stu-id="e5211-133">NOTES</span></span>

## <span data-ttu-id="e5211-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5211-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5211-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5211-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="e5211-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5211-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="e5211-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="e5211-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="e5211-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e5211-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


