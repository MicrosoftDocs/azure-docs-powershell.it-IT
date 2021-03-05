---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: d66203d712de76004d009b98fdc14a18cc69e461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961293"
---
# <span data-ttu-id="34ad4-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="34ad4-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="34ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="34ad4-103">Rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34ad4-103">Removes a storage queue.</span></span>

## <span data-ttu-id="34ad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34ad4-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ad4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="34ad4-106">Il cmdlet **Remove-AzStorageQueue** rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34ad4-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="34ad4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="34ad4-108">Esempio 1: Rimuovere una coda di archiviazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="34ad4-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="34ad4-109">Questo comando rimuove una coda denominata ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="34ad4-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="34ad4-110">Esempio 2: Rimuovere più code di archiviazione</span><span class="sxs-lookup"><span data-stu-id="34ad4-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="34ad4-111">Questo comando rimuove tutte le code con nomi che iniziano con Contoso.</span><span class="sxs-lookup"><span data-stu-id="34ad4-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="34ad4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34ad4-112">PARAMETERS</span></span>

### <span data-ttu-id="34ad4-113">-Context</span><span class="sxs-lookup"><span data-stu-id="34ad4-113">-Context</span></span>
<span data-ttu-id="34ad4-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34ad4-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="34ad4-115">Per ottenere il contesto di archiviazione, il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34ad4-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ad4-116">-DefaultProfile</span></span>
<span data-ttu-id="34ad4-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34ad4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ad4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="34ad4-118">-Force</span></span>
<span data-ttu-id="34ad4-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="34ad4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34ad4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="34ad4-120">-Name</span></span>
<span data-ttu-id="34ad4-121">Specifica il nome della coda da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="34ad4-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ad4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34ad4-122">-PassThru</span></span>
<span data-ttu-id="34ad4-123">Indica che questo cmdlet restituisce un valore **booleano** che riflette il successo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="34ad4-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="34ad4-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="34ad4-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="34ad4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34ad4-125">-Confirm</span></span>
<span data-ttu-id="34ad4-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ad4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ad4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ad4-127">-WhatIf</span></span>
<span data-ttu-id="34ad4-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34ad4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ad4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34ad4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ad4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ad4-130">CommonParameters</span></span>
<span data-ttu-id="34ad4-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ad4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ad4-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ad4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ad4-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="34ad4-133">INPUTS</span></span>

### <span data-ttu-id="34ad4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="34ad4-134">System.String</span></span>

### <span data-ttu-id="34ad4-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34ad4-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34ad4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34ad4-136">OUTPUTS</span></span>

### <span data-ttu-id="34ad4-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34ad4-137">System.Boolean</span></span>

## <span data-ttu-id="34ad4-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="34ad4-138">NOTES</span></span>

## <span data-ttu-id="34ad4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34ad4-139">RELATED LINKS</span></span>

[<span data-ttu-id="34ad4-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="34ad4-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="34ad4-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="34ad4-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
