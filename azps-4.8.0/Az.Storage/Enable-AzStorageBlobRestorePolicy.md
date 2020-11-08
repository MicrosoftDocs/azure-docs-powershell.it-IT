---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033655"
---
# <span data-ttu-id="3b8f1-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8f1-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="3b8f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8f1-103">Abilita i criteri di ripristino BLOB in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="3b8f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b8f1-104">SYNTAX</span></span>

### <span data-ttu-id="3b8f1-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b8f1-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8f1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3b8f1-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b8f1-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="3b8f1-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8f1-108">DESCRIPTION</span></span>
<span data-ttu-id="3b8f1-109">Il cmdlet **Enable-AzStorageBlobRestorePolicy** Abilita i criteri di ripristino BLOB per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="3b8f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b8f1-110">EXAMPLES</span></span>

### <span data-ttu-id="3b8f1-111">Esempio 1: Abilita i criteri di ripristino BLOB per il servizio BLOB di archiviazione di Azure in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3b8f1-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="3b8f1-112">Questo comando Abilita prima BLOB SoftDelete e changefeed, quindi Abilita i criteri di ripristino BLOB, infine controlla l'impostazione nelle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="3b8f1-113">Il servizio BLOB RestorePolicy. Days deve essere minore di DeleteRetentionPolicy. Days.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="3b8f1-114">I BLOB SoftDelete e ChangeFeed devono essere abilitati prima di abilitare i criteri di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="3b8f1-115">Se SoftDelete e changefeed sono solo abilitati, potrebbe essere necessario attendere un po' di tempo prima che il server gestisca l'impostazione, prima di abilitare i criteri di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="3b8f1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b8f1-116">PARAMETERS</span></span>

### <span data-ttu-id="3b8f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8f1-117">-DefaultProfile</span></span>
<span data-ttu-id="3b8f1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b8f1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b8f1-119">-PassThru</span></span>
<span data-ttu-id="3b8f1-120">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="3b8f1-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="3b8f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b8f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b8f1-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3b8f1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b8f1-123">-ResourceId</span></span>
<span data-ttu-id="3b8f1-124">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="3b8f1-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="3b8f1-125">-RestoreDays</span></span>
<span data-ttu-id="3b8f1-126">Imposta il numero di giorni per cui il BLOB può essere ripristinato.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="3b8f1-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b8f1-127">-StorageAccount</span></span>
<span data-ttu-id="3b8f1-128">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3b8f1-128">Storage account object</span></span>

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

### <span data-ttu-id="3b8f1-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3b8f1-129">-StorageAccountName</span></span>
<span data-ttu-id="3b8f1-130">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="3b8f1-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b8f1-131">-Confirm</span></span>
<span data-ttu-id="3b8f1-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b8f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8f1-133">-WhatIf</span></span>
<span data-ttu-id="3b8f1-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b8f1-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b8f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8f1-136">CommonParameters</span></span>
<span data-ttu-id="3b8f1-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8f1-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8f1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8f1-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b8f1-139">INPUTS</span></span>

### <span data-ttu-id="3b8f1-140">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b8f1-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3b8f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3b8f1-141">System.String</span></span>

## <span data-ttu-id="3b8f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b8f1-142">OUTPUTS</span></span>

### <span data-ttu-id="3b8f1-143">Microsoft. Azure. Commands. Management. storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8f1-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="3b8f1-144">Note</span><span class="sxs-lookup"><span data-stu-id="3b8f1-144">NOTES</span></span>

## <span data-ttu-id="3b8f1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b8f1-145">RELATED LINKS</span></span>
