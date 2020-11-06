---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 7784ea832faef9f73b46b04d6ad36bebe0e2f36d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519327"
---
# <span data-ttu-id="293b1-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="293b1-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="293b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="293b1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="293b1-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="293b1-103">SYNTAX</span></span>

### <span data-ttu-id="293b1-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="293b1-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="293b1-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="293b1-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="293b1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="293b1-106">DESCRIPTION</span></span>
<span data-ttu-id="293b1-107">Il cmdlet **New-AzureRmWebAppBackup** crea un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="293b1-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="293b1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="293b1-108">EXAMPLES</span></span>

### <span data-ttu-id="293b1-109">1:</span><span class="sxs-lookup"><span data-stu-id="293b1-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="293b1-110">Crea una copia di backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="293b1-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="293b1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="293b1-111">PARAMETERS</span></span>

### <span data-ttu-id="293b1-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="293b1-112">-BackupName</span></span>
<span data-ttu-id="293b1-113">Nome del backup</span><span class="sxs-lookup"><span data-stu-id="293b1-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293b1-114">-Database</span><span class="sxs-lookup"><span data-stu-id="293b1-114">-Databases</span></span>
<span data-ttu-id="293b1-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="293b1-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="293b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293b1-116">-DefaultProfile</span></span>
<span data-ttu-id="293b1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="293b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293b1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="293b1-118">-Name</span></span>
<span data-ttu-id="293b1-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="293b1-119">WebApp Name</span></span>

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

### <span data-ttu-id="293b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="293b1-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="293b1-121">Resource Group Name</span></span>

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

### <span data-ttu-id="293b1-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="293b1-122">-Slot</span></span>
<span data-ttu-id="293b1-123">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="293b1-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="293b1-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="293b1-124">-StorageAccountUrl</span></span>
<span data-ttu-id="293b1-125">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="293b1-125">Storage Account Url</span></span>

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

### <span data-ttu-id="293b1-126">-Web App</span><span class="sxs-lookup"><span data-stu-id="293b1-126">-WebApp</span></span>
<span data-ttu-id="293b1-127">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="293b1-127">WebApp Object</span></span>

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

### <span data-ttu-id="293b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293b1-128">CommonParameters</span></span>
<span data-ttu-id="293b1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293b1-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293b1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293b1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="293b1-131">INPUTS</span></span>

### <span data-ttu-id="293b1-132">Sito</span><span class="sxs-lookup"><span data-stu-id="293b1-132">Site</span></span>
<span data-ttu-id="293b1-133">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="293b1-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="293b1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="293b1-134">OUTPUTS</span></span>

### <span data-ttu-id="293b1-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="293b1-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="293b1-136">Note</span><span class="sxs-lookup"><span data-stu-id="293b1-136">NOTES</span></span>

## <span data-ttu-id="293b1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="293b1-137">RELATED LINKS</span></span>

