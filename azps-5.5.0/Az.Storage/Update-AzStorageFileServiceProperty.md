---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197470"
---
# <span data-ttu-id="d3f04-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d3f04-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="d3f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f04-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f04-103">Modifica le proprietà del servizio per il servizio File di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f04-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d3f04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3f04-104">SYNTAX</span></span>

### <span data-ttu-id="d3f04-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3f04-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f04-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d3f04-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f04-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f04-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f04-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3f04-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f04-109">Il cmdlet **Update-AzStorageFileServiceProperty** modifica le proprietà del servizio per il servizio File di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f04-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d3f04-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3f04-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f04-111">Esempio 1: Abilitare condivisione file softdelete</span><span class="sxs-lookup"><span data-stu-id="d3f04-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="d3f04-112">Questo comando abilita l'eliminazione softdelete della condivisione file con 5 giorni di conservazione</span><span class="sxs-lookup"><span data-stu-id="d3f04-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="d3f04-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f04-113">PARAMETERS</span></span>

### <span data-ttu-id="d3f04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f04-114">-DefaultProfile</span></span>
<span data-ttu-id="d3f04-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f04-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3f04-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="d3f04-117">Abilitare l'opzione Elimina criteri di conservazione per l'account di archiviazione impostandola su $true, su Elimina criteri di conservazione condivisi impostandolo su $false.</span><span class="sxs-lookup"><span data-stu-id="d3f04-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="d3f04-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f04-118">-ResourceGroupName</span></span>
<span data-ttu-id="d3f04-119">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3f04-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3f04-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f04-120">-ResourceId</span></span>
<span data-ttu-id="d3f04-121">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio file.</span><span class="sxs-lookup"><span data-stu-id="d3f04-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="d3f04-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="d3f04-122">-ShareRetentionDays</span></span>
<span data-ttu-id="d3f04-123">Imposta il numero di giorni di conservazione per la condivisione DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d3f04-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="d3f04-124">Il valore deve essere impostato solo quando si abilita l'opzione Elimina criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="d3f04-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="d3f04-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3f04-125">-StorageAccount</span></span>
<span data-ttu-id="d3f04-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d3f04-126">Storage account object</span></span>

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

### <span data-ttu-id="d3f04-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3f04-127">-StorageAccountName</span></span>
<span data-ttu-id="d3f04-128">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d3f04-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d3f04-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3f04-129">-Confirm</span></span>
<span data-ttu-id="d3f04-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f04-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f04-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f04-131">-WhatIf</span></span>
<span data-ttu-id="d3f04-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3f04-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f04-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3f04-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f04-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f04-134">CommonParameters</span></span>
<span data-ttu-id="d3f04-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f04-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f04-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f04-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f04-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3f04-137">INPUTS</span></span>

### <span data-ttu-id="d3f04-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3f04-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d3f04-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d3f04-139">System.String</span></span>

## <span data-ttu-id="d3f04-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3f04-140">OUTPUTS</span></span>

### <span data-ttu-id="d3f04-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d3f04-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="d3f04-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3f04-142">NOTES</span></span>

## <span data-ttu-id="d3f04-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3f04-143">RELATED LINKS</span></span>
