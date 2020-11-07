---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688209"
---
# <span data-ttu-id="43610-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="43610-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="43610-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43610-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43610-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43610-103">SYNTAX</span></span>

### <span data-ttu-id="43610-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="43610-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="43610-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="43610-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="43610-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43610-106">DESCRIPTION</span></span>
<span data-ttu-id="43610-107">Il cmdlet **New-AzureRmWebAppBackup** crea un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="43610-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="43610-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43610-108">EXAMPLES</span></span>

### <span data-ttu-id="43610-109">1:</span><span class="sxs-lookup"><span data-stu-id="43610-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="43610-110">Crea una copia di backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="43610-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="43610-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43610-111">PARAMETERS</span></span>

### <span data-ttu-id="43610-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="43610-112">-BackupName</span></span>
<span data-ttu-id="43610-113">Nome del backup</span><span class="sxs-lookup"><span data-stu-id="43610-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43610-114">-Database</span><span class="sxs-lookup"><span data-stu-id="43610-114">-Databases</span></span>
<span data-ttu-id="43610-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="43610-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="43610-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="43610-116">-Name</span></span>
<span data-ttu-id="43610-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="43610-117">WebApp Name</span></span>

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

### <span data-ttu-id="43610-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43610-118">-ResourceGroupName</span></span>
<span data-ttu-id="43610-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="43610-119">Resource Group Name</span></span>

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

### <span data-ttu-id="43610-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="43610-120">-Slot</span></span>
<span data-ttu-id="43610-121">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="43610-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="43610-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="43610-122">-StorageAccountUrl</span></span>
<span data-ttu-id="43610-123">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="43610-123">Storage Account Url</span></span>

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

### <span data-ttu-id="43610-124">-Web App</span><span class="sxs-lookup"><span data-stu-id="43610-124">-WebApp</span></span>
<span data-ttu-id="43610-125">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="43610-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43610-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43610-126">-DefaultProfile</span></span>
<span data-ttu-id="43610-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43610-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43610-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43610-128">CommonParameters</span></span>
<span data-ttu-id="43610-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43610-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43610-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43610-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43610-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43610-131">INPUTS</span></span>

### <span data-ttu-id="43610-132">Sito</span><span class="sxs-lookup"><span data-stu-id="43610-132">Site</span></span>
<span data-ttu-id="43610-133">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="43610-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="43610-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43610-134">OUTPUTS</span></span>

### <span data-ttu-id="43610-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="43610-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="43610-136">Note</span><span class="sxs-lookup"><span data-stu-id="43610-136">NOTES</span></span>

## <span data-ttu-id="43610-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43610-137">RELATED LINKS</span></span>

