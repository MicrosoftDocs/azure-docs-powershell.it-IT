---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519804"
---
# <span data-ttu-id="b051f-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b051f-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="b051f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b051f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b051f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b051f-103">SYNTAX</span></span>

### <span data-ttu-id="b051f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b051f-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="b051f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b051f-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="b051f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b051f-106">DESCRIPTION</span></span>
<span data-ttu-id="b051f-107">Il cmdlet **Restore-AzureRmWebAppBackup** ripristina un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b051f-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="b051f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b051f-108">EXAMPLES</span></span>

### <span data-ttu-id="b051f-109">1:</span><span class="sxs-lookup"><span data-stu-id="b051f-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="b051f-110">Ripristina un backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in BLOB "blob" che si trova in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="b051f-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="b051f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b051f-111">PARAMETERS</span></span>

### <span data-ttu-id="b051f-112">-Blobname</span><span class="sxs-lookup"><span data-stu-id="b051f-112">-BlobName</span></span>
<span data-ttu-id="b051f-113">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="b051f-113">Blob Name</span></span>

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

### <span data-ttu-id="b051f-114">-Database</span><span class="sxs-lookup"><span data-stu-id="b051f-114">-Databases</span></span>
<span data-ttu-id="b051f-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="b051f-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="b051f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b051f-116">-DefaultProfile</span></span>
<span data-ttu-id="b051f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b051f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b051f-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="b051f-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="b051f-119">Opzione Ignora nomi host in conflitto</span><span class="sxs-lookup"><span data-stu-id="b051f-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="b051f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b051f-120">-Name</span></span>
<span data-ttu-id="b051f-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b051f-121">WebApp Name</span></span>

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

### <span data-ttu-id="b051f-122">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="b051f-122">-Overwrite</span></span>
<span data-ttu-id="b051f-123">Opzione Sovrascrivi</span><span class="sxs-lookup"><span data-stu-id="b051f-123">Overwrite Option</span></span>

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

### <span data-ttu-id="b051f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b051f-124">-ResourceGroupName</span></span>
<span data-ttu-id="b051f-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b051f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b051f-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="b051f-126">-Slot</span></span>
<span data-ttu-id="b051f-127">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="b051f-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b051f-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b051f-128">-StorageAccountUrl</span></span>
<span data-ttu-id="b051f-129">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b051f-129">Storage Account Url</span></span>

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

### <span data-ttu-id="b051f-130">-Web App</span><span class="sxs-lookup"><span data-stu-id="b051f-130">-WebApp</span></span>
<span data-ttu-id="b051f-131">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="b051f-131">WebApp Object</span></span>

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

### <span data-ttu-id="b051f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b051f-132">CommonParameters</span></span>
<span data-ttu-id="b051f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b051f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b051f-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b051f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b051f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b051f-135">INPUTS</span></span>

### <span data-ttu-id="b051f-136">Sito</span><span class="sxs-lookup"><span data-stu-id="b051f-136">Site</span></span>
<span data-ttu-id="b051f-137">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b051f-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b051f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b051f-138">OUTPUTS</span></span>

## <span data-ttu-id="b051f-139">Note</span><span class="sxs-lookup"><span data-stu-id="b051f-139">NOTES</span></span>

## <span data-ttu-id="b051f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b051f-140">RELATED LINKS</span></span>
