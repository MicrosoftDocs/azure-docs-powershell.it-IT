---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861905"
---
# <span data-ttu-id="7a778-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7a778-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="7a778-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a778-102">SYNOPSIS</span></span>

## <span data-ttu-id="7a778-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a778-103">SYNTAX</span></span>

### <span data-ttu-id="7a778-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7a778-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="7a778-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7a778-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="7a778-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a778-106">DESCRIPTION</span></span>
<span data-ttu-id="7a778-107">Il cmdlet **New-AzWebAppBackup** crea un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7a778-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="7a778-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a778-108">EXAMPLES</span></span>

### <span data-ttu-id="7a778-109">1:</span><span class="sxs-lookup"><span data-stu-id="7a778-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="7a778-110">Crea una copia di backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="7a778-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="7a778-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a778-111">PARAMETERS</span></span>

### <span data-ttu-id="7a778-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="7a778-112">-BackupName</span></span>
<span data-ttu-id="7a778-113">Nome del backup</span><span class="sxs-lookup"><span data-stu-id="7a778-113">Backup Name</span></span>

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

### <span data-ttu-id="7a778-114">-Database</span><span class="sxs-lookup"><span data-stu-id="7a778-114">-Databases</span></span>
<span data-ttu-id="7a778-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="7a778-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="7a778-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a778-116">-DefaultProfile</span></span>
<span data-ttu-id="7a778-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a778-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a778-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a778-118">-Name</span></span>
<span data-ttu-id="7a778-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="7a778-119">WebApp Name</span></span>

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

### <span data-ttu-id="7a778-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a778-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a778-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7a778-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7a778-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="7a778-122">-Slot</span></span>
<span data-ttu-id="7a778-123">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="7a778-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7a778-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7a778-124">-StorageAccountUrl</span></span>
<span data-ttu-id="7a778-125">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7a778-125">Storage Account Url</span></span>

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

### <span data-ttu-id="7a778-126">-Web App</span><span class="sxs-lookup"><span data-stu-id="7a778-126">-WebApp</span></span>
<span data-ttu-id="7a778-127">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="7a778-127">WebApp Object</span></span>

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

### <span data-ttu-id="7a778-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a778-128">CommonParameters</span></span>
<span data-ttu-id="7a778-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a778-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a778-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a778-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a778-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a778-131">INPUTS</span></span>

### <span data-ttu-id="7a778-132">Sito</span><span class="sxs-lookup"><span data-stu-id="7a778-132">Site</span></span>
<span data-ttu-id="7a778-133">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a778-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7a778-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a778-134">OUTPUTS</span></span>

### <span data-ttu-id="7a778-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7a778-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="7a778-136">Note</span><span class="sxs-lookup"><span data-stu-id="7a778-136">NOTES</span></span>

## <span data-ttu-id="7a778-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a778-137">RELATED LINKS</span></span>

