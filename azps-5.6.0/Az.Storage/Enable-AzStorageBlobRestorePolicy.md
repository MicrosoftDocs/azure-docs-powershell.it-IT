---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973342"
---
# <span data-ttu-id="87303-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="87303-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="87303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87303-102">SYNOPSIS</span></span>
<span data-ttu-id="87303-103">Abilita i criteri di ripristino BLOB in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="87303-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="87303-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87303-104">SYNTAX</span></span>

### <span data-ttu-id="87303-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87303-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87303-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="87303-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87303-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="87303-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87303-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87303-108">DESCRIPTION</span></span>
<span data-ttu-id="87303-109">Il cmdlet **Enable-AzStorageBlobRestorePolicy** abilita i criteri di ripristino blob per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="87303-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="87303-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87303-110">EXAMPLES</span></span>

### <span data-ttu-id="87303-111">Esempio 1: Abilita i criteri di Ripristino BLOB per il servizio BLOB Archiviazione di Azure in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="87303-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="87303-112">Questo comando abilita prima softdelete BLOB e changefeed, quindi abilita Criteri di ripristino BLOB e infine controlla l'impostazione nelle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="87303-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="87303-113">Il valore di RestorePolicy del servizio BLOB.Days deve essere minore di DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="87303-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="87303-114">Blob softdelete e ChangeFeed devono essere abilitati prima di abilitare i criteri di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="87303-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="87303-115">Se le opzioni softdelete e changefeed sono appena abilitate, potrebbe essere necessario attendere del tempo prima che il server gestirà l'impostazione prima di abilitare i criteri di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="87303-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="87303-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87303-116">PARAMETERS</span></span>

### <span data-ttu-id="87303-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87303-117">-DefaultProfile</span></span>
<span data-ttu-id="87303-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87303-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87303-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87303-119">-PassThru</span></span>
<span data-ttu-id="87303-120">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="87303-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="87303-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87303-121">-ResourceGroupName</span></span>
<span data-ttu-id="87303-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87303-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="87303-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87303-123">-ResourceId</span></span>
<span data-ttu-id="87303-124">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="87303-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87303-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="87303-125">-RestoreDays</span></span>
<span data-ttu-id="87303-126">Imposta il numero di giorni per cui è possibile ripristinare il BLOB.</span><span class="sxs-lookup"><span data-stu-id="87303-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87303-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="87303-127">-StorageAccount</span></span>
<span data-ttu-id="87303-128">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="87303-128">Storage account object</span></span>

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

### <span data-ttu-id="87303-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87303-129">-StorageAccountName</span></span>
<span data-ttu-id="87303-130">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="87303-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87303-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87303-131">-Confirm</span></span>
<span data-ttu-id="87303-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87303-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87303-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87303-133">-WhatIf</span></span>
<span data-ttu-id="87303-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87303-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87303-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87303-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87303-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87303-136">CommonParameters</span></span>
<span data-ttu-id="87303-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87303-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87303-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87303-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87303-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="87303-139">INPUTS</span></span>

### <span data-ttu-id="87303-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87303-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="87303-141">System.String</span><span class="sxs-lookup"><span data-stu-id="87303-141">System.String</span></span>

## <span data-ttu-id="87303-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87303-142">OUTPUTS</span></span>

### <span data-ttu-id="87303-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="87303-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="87303-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="87303-144">NOTES</span></span>

## <span data-ttu-id="87303-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87303-145">RELATED LINKS</span></span>
