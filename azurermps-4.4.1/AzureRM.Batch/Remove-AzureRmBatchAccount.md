---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3de75d2c8e7ed69a8f5be02833dd002ee5fbf016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519215"
---
# <span data-ttu-id="9bd74-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bd74-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="9bd74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bd74-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd74-103">Rimuove un account batch.</span><span class="sxs-lookup"><span data-stu-id="9bd74-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bd74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bd74-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bd74-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd74-106">Il cmdlet **Remove-AzureRmBatchAccount** rimuove un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd74-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="9bd74-107">Questo cmdlet richiede prima che venga rimosso un account, a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="9bd74-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="9bd74-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bd74-108">EXAMPLES</span></span>

### <span data-ttu-id="9bd74-109">Esempio 1: rimuovere un account batch</span><span class="sxs-lookup"><span data-stu-id="9bd74-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="9bd74-110">Questo comando consente di rimuovere l'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="9bd74-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="9bd74-111">Questo comando richiede conferma prima di eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="9bd74-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="9bd74-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bd74-112">PARAMETERS</span></span>

### <span data-ttu-id="9bd74-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9bd74-113">-AccountName</span></span>
<span data-ttu-id="9bd74-114">Specifica il nome dell'account batch rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd74-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bd74-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9bd74-115">-Force</span></span>
<span data-ttu-id="9bd74-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9bd74-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bd74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd74-117">-ResourceGroupName</span></span>
<span data-ttu-id="9bd74-118">Specifica il gruppo di risorse dell'account rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd74-118">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bd74-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bd74-119">-Confirm</span></span>
<span data-ttu-id="9bd74-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd74-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd74-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd74-121">-WhatIf</span></span>
<span data-ttu-id="9bd74-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bd74-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd74-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bd74-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd74-124">-DefaultProfile</span></span>
<span data-ttu-id="9bd74-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd74-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd74-126">CommonParameters</span></span>
<span data-ttu-id="9bd74-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd74-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd74-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd74-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bd74-129">INPUTS</span></span>

## <span data-ttu-id="9bd74-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bd74-130">OUTPUTS</span></span>

## <span data-ttu-id="9bd74-131">Note</span><span class="sxs-lookup"><span data-stu-id="9bd74-131">NOTES</span></span>

## <span data-ttu-id="9bd74-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bd74-132">RELATED LINKS</span></span>

[<span data-ttu-id="9bd74-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bd74-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="9bd74-134">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bd74-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="9bd74-135">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bd74-135">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="9bd74-136">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="9bd74-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

