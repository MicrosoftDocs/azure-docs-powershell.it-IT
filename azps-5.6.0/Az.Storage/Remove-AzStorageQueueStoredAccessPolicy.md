---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961277"
---
# <span data-ttu-id="b06c4-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b06c4-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="b06c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b06c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b06c4-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06c4-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="b06c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b06c4-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b06c4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b06c4-105">DESCRIPTION</span></span>
<span data-ttu-id="b06c4-106">Il cmdlet **Remove-AzStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06c4-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="b06c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b06c4-107">EXAMPLES</span></span>

### <span data-ttu-id="b06c4-108">Esempio 1: Rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b06c4-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="b06c4-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="b06c4-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="b06c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b06c4-110">PARAMETERS</span></span>

### <span data-ttu-id="b06c4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b06c4-111">-Context</span></span>
<span data-ttu-id="b06c4-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06c4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b06c4-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b06c4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b06c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06c4-114">-DefaultProfile</span></span>
<span data-ttu-id="b06c4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b06c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06c4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b06c4-116">-PassThru</span></span>
<span data-ttu-id="b06c4-117">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b06c4-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b06c4-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b06c4-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b06c4-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="b06c4-119">-Policy</span></span>
<span data-ttu-id="b06c4-120">Specifica il nome dei criteri di accesso archiviato rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b06c4-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06c4-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="b06c4-121">-Queue</span></span>
<span data-ttu-id="b06c4-122">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b06c4-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06c4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b06c4-123">-Confirm</span></span>
<span data-ttu-id="b06c4-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b06c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b06c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b06c4-125">-WhatIf</span></span>
<span data-ttu-id="b06c4-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b06c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b06c4-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b06c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b06c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06c4-128">CommonParameters</span></span>
<span data-ttu-id="b06c4-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06c4-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b06c4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06c4-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b06c4-131">INPUTS</span></span>

### <span data-ttu-id="b06c4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b06c4-132">System.String</span></span>

### <span data-ttu-id="b06c4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b06c4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b06c4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b06c4-134">OUTPUTS</span></span>

### <span data-ttu-id="b06c4-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b06c4-135">System.Boolean</span></span>

## <span data-ttu-id="b06c4-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="b06c4-136">NOTES</span></span>

## <span data-ttu-id="b06c4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b06c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="b06c4-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b06c4-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b06c4-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b06c4-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b06c4-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b06c4-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b06c4-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b06c4-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
