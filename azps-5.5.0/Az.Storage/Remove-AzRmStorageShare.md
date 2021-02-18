---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190783"
---
# <span data-ttu-id="94088-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94088-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="94088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94088-102">SYNOPSIS</span></span>
<span data-ttu-id="94088-103">Rimuove una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94088-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="94088-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94088-104">SYNTAX</span></span>

### <span data-ttu-id="94088-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94088-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94088-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="94088-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94088-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="94088-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94088-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="94088-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94088-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94088-109">DESCRIPTION</span></span>
<span data-ttu-id="94088-110">Il cmdlet **New-AzRmStorageShare** rimuove una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94088-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="94088-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94088-111">EXAMPLES</span></span>

### <span data-ttu-id="94088-112">Esempio 1: Rimuovere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="94088-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="94088-113">Questo comando rimuove una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="94088-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="94088-114">Esempio 2: Rimuovere una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="94088-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="94088-115">Questo comando rimuove una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="94088-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="94088-116">Esempio 3: Rimuovere tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="94088-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="94088-117">Questo comando rimuove tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="94088-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="94088-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94088-118">PARAMETERS</span></span>

### <span data-ttu-id="94088-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94088-119">-DefaultProfile</span></span>
<span data-ttu-id="94088-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94088-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94088-121">-Force</span><span class="sxs-lookup"><span data-stu-id="94088-121">-Force</span></span>
<span data-ttu-id="94088-122">Forzare la rimozione della condivisione e di tutto il contenuto in essa contenuto</span><span class="sxs-lookup"><span data-stu-id="94088-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="94088-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94088-123">-InputObject</span></span>
<span data-ttu-id="94088-124">Oggetto Condivisione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="94088-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94088-125">-Name</span><span class="sxs-lookup"><span data-stu-id="94088-125">-Name</span></span>
<span data-ttu-id="94088-126">Condividi nome</span><span class="sxs-lookup"><span data-stu-id="94088-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94088-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94088-127">-PassThru</span></span>
<span data-ttu-id="94088-128">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="94088-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="94088-129">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="94088-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="94088-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94088-130">-ResourceGroupName</span></span>
<span data-ttu-id="94088-131">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94088-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94088-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94088-132">-ResourceId</span></span>
<span data-ttu-id="94088-133">Immettere un ID di risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="94088-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94088-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="94088-134">-StorageAccount</span></span>
<span data-ttu-id="94088-135">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="94088-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94088-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94088-136">-StorageAccountName</span></span>
<span data-ttu-id="94088-137">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94088-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94088-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94088-138">-Confirm</span></span>
<span data-ttu-id="94088-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94088-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94088-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94088-140">-WhatIf</span></span>
<span data-ttu-id="94088-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94088-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94088-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94088-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94088-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94088-143">CommonParameters</span></span>
<span data-ttu-id="94088-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94088-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94088-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94088-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94088-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="94088-146">INPUTS</span></span>

### <span data-ttu-id="94088-147">System.String</span><span class="sxs-lookup"><span data-stu-id="94088-147">System.String</span></span>

### <span data-ttu-id="94088-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94088-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="94088-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="94088-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="94088-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94088-150">OUTPUTS</span></span>

### <span data-ttu-id="94088-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94088-151">System.Boolean</span></span>

## <span data-ttu-id="94088-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="94088-152">NOTES</span></span>

## <span data-ttu-id="94088-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94088-153">RELATED LINKS</span></span>
