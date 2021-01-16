---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374146"
---
# <span data-ttu-id="47229-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="47229-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="47229-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47229-102">SYNOPSIS</span></span>
<span data-ttu-id="47229-103">Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="47229-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="47229-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47229-104">SYNTAX</span></span>

### <span data-ttu-id="47229-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47229-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47229-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="47229-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47229-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="47229-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47229-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47229-108">DESCRIPTION</span></span>
<span data-ttu-id="47229-109">Il cmdlet **Enable-AzStorageBlobDeleteRetentionPolicy** consente di eliminare i criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="47229-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="47229-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47229-110">EXAMPLES</span></span>

### <span data-ttu-id="47229-111">Esempio 1: abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="47229-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="47229-112">Questo comando consente di eliminare i criteri di conservazione per il servizio BLOB e di impostare i giorni di conservazione BLOB eliminati su 4.</span><span class="sxs-lookup"><span data-stu-id="47229-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="47229-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47229-113">PARAMETERS</span></span>

### <span data-ttu-id="47229-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47229-114">-DefaultProfile</span></span>
<span data-ttu-id="47229-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47229-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47229-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47229-116">-PassThru</span></span>
<span data-ttu-id="47229-117">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="47229-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="47229-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47229-118">-ResourceGroupName</span></span>
<span data-ttu-id="47229-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47229-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="47229-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47229-120">-ResourceId</span></span>
<span data-ttu-id="47229-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="47229-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="47229-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="47229-122">-RetentionDays</span></span>
<span data-ttu-id="47229-123">Imposta il numero di giorni di conservazione per DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="47229-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="47229-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="47229-124">-StorageAccount</span></span>
<span data-ttu-id="47229-125">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="47229-125">Storage account object</span></span>

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

### <span data-ttu-id="47229-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47229-126">-StorageAccountName</span></span>
<span data-ttu-id="47229-127">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="47229-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="47229-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47229-128">-Confirm</span></span>
<span data-ttu-id="47229-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47229-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47229-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47229-130">-WhatIf</span></span>
<span data-ttu-id="47229-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47229-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47229-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47229-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47229-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47229-133">CommonParameters</span></span>
<span data-ttu-id="47229-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47229-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47229-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47229-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47229-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47229-136">INPUTS</span></span>

### <span data-ttu-id="47229-137">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47229-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="47229-138">System. String</span><span class="sxs-lookup"><span data-stu-id="47229-138">System.String</span></span>

## <span data-ttu-id="47229-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47229-139">OUTPUTS</span></span>

### <span data-ttu-id="47229-140">Microsoft. Azure. Commands. Management. storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="47229-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="47229-141">Note</span><span class="sxs-lookup"><span data-stu-id="47229-141">NOTES</span></span>

## <span data-ttu-id="47229-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47229-142">RELATED LINKS</span></span>
