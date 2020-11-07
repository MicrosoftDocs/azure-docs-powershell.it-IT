---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866786"
---
# <span data-ttu-id="51b05-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="51b05-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="51b05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51b05-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b05-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51b05-103">SYNTAX</span></span>

### <span data-ttu-id="51b05-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="51b05-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="51b05-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="51b05-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="51b05-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51b05-106">DESCRIPTION</span></span>
<span data-ttu-id="51b05-107">Il cmdlet **Restore-AzureRmWebAppBackup** ripristina un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="51b05-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="51b05-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51b05-108">EXAMPLES</span></span>

### <span data-ttu-id="51b05-109">1:</span><span class="sxs-lookup"><span data-stu-id="51b05-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="51b05-110">Ripristina un backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in BLOB "blob" che si trova in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="51b05-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="51b05-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51b05-111">PARAMETERS</span></span>

### <span data-ttu-id="51b05-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="51b05-112">-AppServicePlan</span></span>
<span data-ttu-id="51b05-113">Il nome del piano del servizio app per l'app ripristinata.</span><span class="sxs-lookup"><span data-stu-id="51b05-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="51b05-114">Se lasciato vuoto, viene usato il piano di servizio corrente dell'app.</span><span class="sxs-lookup"><span data-stu-id="51b05-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="51b05-115">-BlobName</span></span>
<span data-ttu-id="51b05-116">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="51b05-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-117">-Database</span><span class="sxs-lookup"><span data-stu-id="51b05-117">-Databases</span></span>
<span data-ttu-id="51b05-118">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="51b05-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b05-119">-DefaultProfile</span></span>
<span data-ttu-id="51b05-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51b05-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="51b05-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="51b05-122">Opzione Ignora nomi host in conflitto</span><span class="sxs-lookup"><span data-stu-id="51b05-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="51b05-123">-Name</span></span>
<span data-ttu-id="51b05-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="51b05-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="51b05-125">-Overwrite</span></span>
<span data-ttu-id="51b05-126">Opzione Sovrascrivi</span><span class="sxs-lookup"><span data-stu-id="51b05-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b05-127">-ResourceGroupName</span></span>
<span data-ttu-id="51b05-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="51b05-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="51b05-129">-Slot</span></span>
<span data-ttu-id="51b05-130">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="51b05-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="51b05-131">-StorageAccountUrl</span></span>
<span data-ttu-id="51b05-132">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="51b05-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-133">-Web App</span><span class="sxs-lookup"><span data-stu-id="51b05-133">-WebApp</span></span>
<span data-ttu-id="51b05-134">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="51b05-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b05-135">CommonParameters</span></span>
<span data-ttu-id="51b05-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b05-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b05-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b05-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51b05-138">INPUTS</span></span>

### <span data-ttu-id="51b05-139">Sito</span><span class="sxs-lookup"><span data-stu-id="51b05-139">Site</span></span>
<span data-ttu-id="51b05-140">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="51b05-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="51b05-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51b05-141">OUTPUTS</span></span>

## <span data-ttu-id="51b05-142">Note</span><span class="sxs-lookup"><span data-stu-id="51b05-142">NOTES</span></span>

## <span data-ttu-id="51b05-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51b05-143">RELATED LINKS</span></span>

