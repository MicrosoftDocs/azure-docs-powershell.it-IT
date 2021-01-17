---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474632"
---
# <span data-ttu-id="f4dfc-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f4dfc-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="f4dfc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dfc-103">Modifica le proprietà del servizio per il servizio file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="f4dfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4dfc-104">SYNTAX</span></span>

### <span data-ttu-id="f4dfc-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4dfc-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dfc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f4dfc-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dfc-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dfc-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4dfc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4dfc-108">DESCRIPTION</span></span>
<span data-ttu-id="f4dfc-109">Il cmdlet **Update-AzStorageFileServiceProperty** modifica le proprietà del servizio per il servizio file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="f4dfc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="f4dfc-111">Esempio 1: abilitare la condivisione di file SoftDelete</span><span class="sxs-lookup"><span data-stu-id="f4dfc-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="f4dfc-112">Questo comando consente di eliminare la condivisione di file SoftDelete con i giorni di conservazione come 5</span><span class="sxs-lookup"><span data-stu-id="f4dfc-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="f4dfc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4dfc-113">PARAMETERS</span></span>

### <span data-ttu-id="f4dfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dfc-114">-DefaultProfile</span></span>
<span data-ttu-id="f4dfc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4dfc-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4dfc-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="f4dfc-117">Abilitare la condivisione eliminare i criteri di conservazione per l'account di archiviazione impostando su $true, disabilitare i criteri di conservazione della condivisione Elimina impostando su $false.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dfc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dfc-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4dfc-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f4dfc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dfc-120">-ResourceId</span></span>
<span data-ttu-id="f4dfc-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio file.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dfc-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="f4dfc-122">-ShareRetentionDays</span></span>
<span data-ttu-id="f4dfc-123">Imposta il numero di giorni di conservazione per la condivisione DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="f4dfc-124">Il valore deve essere impostato solo quando si Abilita la condivisione Elimina criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dfc-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4dfc-125">-StorageAccount</span></span>
<span data-ttu-id="f4dfc-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f4dfc-126">Storage account object</span></span>

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

### <span data-ttu-id="f4dfc-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f4dfc-127">-StorageAccountName</span></span>
<span data-ttu-id="f4dfc-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="f4dfc-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4dfc-129">-Confirm</span></span>
<span data-ttu-id="f4dfc-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4dfc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4dfc-131">-WhatIf</span></span>
<span data-ttu-id="f4dfc-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4dfc-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4dfc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dfc-134">CommonParameters</span></span>
<span data-ttu-id="f4dfc-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dfc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dfc-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4dfc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dfc-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4dfc-137">INPUTS</span></span>

### <span data-ttu-id="f4dfc-138">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4dfc-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f4dfc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4dfc-139">System.String</span></span>

## <span data-ttu-id="f4dfc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4dfc-140">OUTPUTS</span></span>

### <span data-ttu-id="f4dfc-141">Microsoft. Azure. Commands. Management. storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f4dfc-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="f4dfc-142">Note</span><span class="sxs-lookup"><span data-stu-id="f4dfc-142">NOTES</span></span>

## <span data-ttu-id="f4dfc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4dfc-143">RELATED LINKS</span></span>
