---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 20d859782081991badab5fc9377fb69beb9550ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020861"
---
# <span data-ttu-id="ef240-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ef240-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="ef240-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef240-102">SYNOPSIS</span></span>

## <span data-ttu-id="ef240-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef240-103">SYNTAX</span></span>

### <span data-ttu-id="ef240-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ef240-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="ef240-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ef240-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="ef240-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef240-106">DESCRIPTION</span></span>
<span data-ttu-id="ef240-107">Il cmdlet **Restore-AzWebAppBackup** ripristina un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ef240-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="ef240-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef240-108">EXAMPLES</span></span>

### <span data-ttu-id="ef240-109">1:</span><span class="sxs-lookup"><span data-stu-id="ef240-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="ef240-110">Ripristina un backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in BLOB "blob" che si trova in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ef240-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ef240-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef240-111">PARAMETERS</span></span>

### <span data-ttu-id="ef240-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef240-112">-AppServicePlan</span></span>
<span data-ttu-id="ef240-113">Il nome del piano del servizio app per l'app ripristinata.</span><span class="sxs-lookup"><span data-stu-id="ef240-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="ef240-114">Se lasciato vuoto, viene usato il piano di servizio corrente dell'app.</span><span class="sxs-lookup"><span data-stu-id="ef240-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="ef240-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="ef240-115">-BlobName</span></span>
<span data-ttu-id="ef240-116">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="ef240-116">Blob Name</span></span>

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

### <span data-ttu-id="ef240-117">-Database</span><span class="sxs-lookup"><span data-stu-id="ef240-117">-Databases</span></span>
<span data-ttu-id="ef240-118">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ef240-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ef240-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef240-119">-DefaultProfile</span></span>
<span data-ttu-id="ef240-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef240-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef240-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="ef240-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="ef240-122">Opzione Ignora nomi host in conflitto</span><span class="sxs-lookup"><span data-stu-id="ef240-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="ef240-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef240-123">-Name</span></span>
<span data-ttu-id="ef240-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ef240-124">WebApp Name</span></span>

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

### <span data-ttu-id="ef240-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="ef240-125">-Overwrite</span></span>
<span data-ttu-id="ef240-126">Opzione Sovrascrivi</span><span class="sxs-lookup"><span data-stu-id="ef240-126">Overwrite Option</span></span>

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

### <span data-ttu-id="ef240-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef240-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef240-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ef240-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ef240-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="ef240-129">-Slot</span></span>
<span data-ttu-id="ef240-130">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ef240-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ef240-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ef240-131">-StorageAccountUrl</span></span>
<span data-ttu-id="ef240-132">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ef240-132">Storage Account Url</span></span>

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

### <span data-ttu-id="ef240-133">-Web App</span><span class="sxs-lookup"><span data-stu-id="ef240-133">-WebApp</span></span>
<span data-ttu-id="ef240-134">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ef240-134">WebApp Object</span></span>

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

### <span data-ttu-id="ef240-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef240-135">CommonParameters</span></span>
<span data-ttu-id="ef240-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef240-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef240-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef240-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef240-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef240-138">INPUTS</span></span>

### <span data-ttu-id="ef240-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ef240-139">System.String</span></span>

### <span data-ttu-id="ef240-140">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ef240-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="ef240-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef240-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ef240-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ef240-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ef240-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef240-143">OUTPUTS</span></span>

### <span data-ttu-id="ef240-144">System. void</span><span class="sxs-lookup"><span data-stu-id="ef240-144">System.Void</span></span>

## <span data-ttu-id="ef240-145">Note</span><span class="sxs-lookup"><span data-stu-id="ef240-145">NOTES</span></span>

## <span data-ttu-id="ef240-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef240-146">RELATED LINKS</span></span>
