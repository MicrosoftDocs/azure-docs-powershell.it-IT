---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198407"
---
# <span data-ttu-id="efe2c-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efe2c-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="efe2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efe2c-102">SYNOPSIS</span></span>
<span data-ttu-id="efe2c-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efe2c-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="efe2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efe2c-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efe2c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="efe2c-105">DESCRIPTION</span></span>
<span data-ttu-id="efe2c-106">Il cmdlet **Remove-AzStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efe2c-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="efe2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efe2c-107">EXAMPLES</span></span>

### <span data-ttu-id="efe2c-108">Esempio 1: Rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="efe2c-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="efe2c-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="efe2c-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="efe2c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efe2c-110">PARAMETERS</span></span>

### <span data-ttu-id="efe2c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="efe2c-111">-Context</span></span>
<span data-ttu-id="efe2c-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efe2c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="efe2c-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="efe2c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="efe2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe2c-114">-DefaultProfile</span></span>
<span data-ttu-id="efe2c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efe2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efe2c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efe2c-116">-PassThru</span></span>
<span data-ttu-id="efe2c-117">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="efe2c-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="efe2c-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="efe2c-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="efe2c-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="efe2c-119">-Policy</span></span>
<span data-ttu-id="efe2c-120">Specifica il nome dei criteri di accesso archiviato rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efe2c-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="efe2c-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="efe2c-121">-Queue</span></span>
<span data-ttu-id="efe2c-122">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efe2c-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="efe2c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efe2c-123">-Confirm</span></span>
<span data-ttu-id="efe2c-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efe2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe2c-125">-WhatIf</span></span>
<span data-ttu-id="efe2c-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe2c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe2c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe2c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe2c-128">CommonParameters</span></span>
<span data-ttu-id="efe2c-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe2c-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe2c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe2c-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="efe2c-131">INPUTS</span></span>

### <span data-ttu-id="efe2c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="efe2c-132">System.String</span></span>

### <span data-ttu-id="efe2c-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="efe2c-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="efe2c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efe2c-134">OUTPUTS</span></span>

### <span data-ttu-id="efe2c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efe2c-135">System.Boolean</span></span>

## <span data-ttu-id="efe2c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="efe2c-136">NOTES</span></span>

## <span data-ttu-id="efe2c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efe2c-137">RELATED LINKS</span></span>

[<span data-ttu-id="efe2c-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efe2c-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="efe2c-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="efe2c-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="efe2c-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efe2c-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="efe2c-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efe2c-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
