---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190024"
---
# <span data-ttu-id="84d5b-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="84d5b-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="84d5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="84d5b-103">Rimuove una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="84d5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d5b-104">SYNTAX</span></span>

### <span data-ttu-id="84d5b-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d5b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d5b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="84d5b-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d5b-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="84d5b-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d5b-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="84d5b-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d5b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d5b-109">DESCRIPTION</span></span>
<span data-ttu-id="84d5b-110">Il cmdlet **New-AzRmStorageShare** rimuove una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="84d5b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d5b-111">EXAMPLES</span></span>

### <span data-ttu-id="84d5b-112">Esempio 1: rimuovere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="84d5b-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="84d5b-113">Questo comando rimuove una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="84d5b-114">Esempio 2: rimuovere una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="84d5b-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="84d5b-115">Questo comando rimuove una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="84d5b-116">Esempio 3: rimuovere tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="84d5b-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="84d5b-117">Questo comando rimuove tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="84d5b-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="84d5b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d5b-118">PARAMETERS</span></span>

### <span data-ttu-id="84d5b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d5b-119">-DefaultProfile</span></span>
<span data-ttu-id="84d5b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d5b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d5b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="84d5b-121">-Force</span></span>
<span data-ttu-id="84d5b-122">Forza per rimuovere la condivisione e tutto il contenuto</span><span class="sxs-lookup"><span data-stu-id="84d5b-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="84d5b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d5b-123">-InputObject</span></span>
<span data-ttu-id="84d5b-124">Oggetto condivisione archiviazione</span><span class="sxs-lookup"><span data-stu-id="84d5b-124">Storage Share object</span></span>

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

### <span data-ttu-id="84d5b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="84d5b-125">-Name</span></span>
<span data-ttu-id="84d5b-126">Nome condivisione</span><span class="sxs-lookup"><span data-stu-id="84d5b-126">Share Name</span></span>

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

### <span data-ttu-id="84d5b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d5b-127">-PassThru</span></span>
<span data-ttu-id="84d5b-128">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="84d5b-129">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="84d5b-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="84d5b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d5b-130">-ResourceGroupName</span></span>
<span data-ttu-id="84d5b-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84d5b-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="84d5b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d5b-132">-ResourceId</span></span>
<span data-ttu-id="84d5b-133">Immettere un ID risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="84d5b-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="84d5b-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="84d5b-134">-StorageAccount</span></span>
<span data-ttu-id="84d5b-135">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="84d5b-135">Storage account object</span></span>

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

### <span data-ttu-id="84d5b-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84d5b-136">-StorageAccountName</span></span>
<span data-ttu-id="84d5b-137">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84d5b-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="84d5b-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84d5b-138">-Confirm</span></span>
<span data-ttu-id="84d5b-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d5b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d5b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d5b-140">-WhatIf</span></span>
<span data-ttu-id="84d5b-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d5b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d5b-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d5b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d5b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d5b-143">CommonParameters</span></span>
<span data-ttu-id="84d5b-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d5b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d5b-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d5b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d5b-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d5b-146">INPUTS</span></span>

### <span data-ttu-id="84d5b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="84d5b-147">System.String</span></span>

### <span data-ttu-id="84d5b-148">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="84d5b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="84d5b-149">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="84d5b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="84d5b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d5b-150">OUTPUTS</span></span>

### <span data-ttu-id="84d5b-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84d5b-151">System.Boolean</span></span>

## <span data-ttu-id="84d5b-152">Note</span><span class="sxs-lookup"><span data-stu-id="84d5b-152">NOTES</span></span>

## <span data-ttu-id="84d5b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d5b-153">RELATED LINKS</span></span>
