---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516303"
---
# <span data-ttu-id="92ef0-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="92ef0-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="92ef0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92ef0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ef0-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92ef0-103">SYNTAX</span></span>

### <span data-ttu-id="92ef0-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="92ef0-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="92ef0-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="92ef0-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="92ef0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92ef0-106">DESCRIPTION</span></span>
<span data-ttu-id="92ef0-107">Il cmdlet **Restore-AzureRmWebAppBackup** ripristina un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="92ef0-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="92ef0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92ef0-108">EXAMPLES</span></span>

### <span data-ttu-id="92ef0-109">1:</span><span class="sxs-lookup"><span data-stu-id="92ef0-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="92ef0-110">Ripristina un backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in BLOB "blob" che si trova in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="92ef0-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="92ef0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92ef0-111">PARAMETERS</span></span>

### <span data-ttu-id="92ef0-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92ef0-112">-AppServicePlan</span></span>
<span data-ttu-id="92ef0-113">Il nome del piano del servizio app per l'app ripristinata.</span><span class="sxs-lookup"><span data-stu-id="92ef0-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="92ef0-114">Se lasciato vuoto, viene usato il piano di servizio corrente dell'app.</span><span class="sxs-lookup"><span data-stu-id="92ef0-114">If left empty, the app's current App Service Plan is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="92ef0-115">-BlobName</span></span>
<span data-ttu-id="92ef0-116">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="92ef0-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-117">-Database</span><span class="sxs-lookup"><span data-stu-id="92ef0-117">-Databases</span></span>
<span data-ttu-id="92ef0-118">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="92ef0-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ef0-119">-DefaultProfile</span></span>
<span data-ttu-id="92ef0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92ef0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="92ef0-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="92ef0-122">Opzione Ignora nomi host in conflitto</span><span class="sxs-lookup"><span data-stu-id="92ef0-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="92ef0-123">-Name</span></span>
<span data-ttu-id="92ef0-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="92ef0-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="92ef0-125">-Overwrite</span></span>
<span data-ttu-id="92ef0-126">Opzione Sovrascrivi</span><span class="sxs-lookup"><span data-stu-id="92ef0-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ef0-127">-ResourceGroupName</span></span>
<span data-ttu-id="92ef0-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="92ef0-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="92ef0-129">-Slot</span></span>
<span data-ttu-id="92ef0-130">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="92ef0-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="92ef0-131">-StorageAccountUrl</span></span>
<span data-ttu-id="92ef0-132">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="92ef0-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-133">-Web App</span><span class="sxs-lookup"><span data-stu-id="92ef0-133">-WebApp</span></span>
<span data-ttu-id="92ef0-134">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="92ef0-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92ef0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ef0-135">CommonParameters</span></span>
<span data-ttu-id="92ef0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92ef0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ef0-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ef0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ef0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92ef0-138">INPUTS</span></span>

### <span data-ttu-id="92ef0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="92ef0-139">System.String</span></span>

### <span data-ttu-id="92ef0-140">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="92ef0-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="92ef0-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92ef0-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="92ef0-142">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="92ef0-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="92ef0-143">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92ef0-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="92ef0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92ef0-144">OUTPUTS</span></span>

### <span data-ttu-id="92ef0-145">System. void</span><span class="sxs-lookup"><span data-stu-id="92ef0-145">System.Void</span></span>

## <span data-ttu-id="92ef0-146">Note</span><span class="sxs-lookup"><span data-stu-id="92ef0-146">NOTES</span></span>

## <span data-ttu-id="92ef0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92ef0-147">RELATED LINKS</span></span>
