---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866169"
---
# <span data-ttu-id="2aaf0-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="2aaf0-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="2aaf0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2aaf0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aaf0-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aaf0-103">SYNTAX</span></span>

### <span data-ttu-id="2aaf0-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2aaf0-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="2aaf0-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaf0-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="2aaf0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aaf0-106">DESCRIPTION</span></span>
<span data-ttu-id="2aaf0-107">Il cmdlet **New-AzureRmWebAppBackup** crea un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="2aaf0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aaf0-108">EXAMPLES</span></span>

### <span data-ttu-id="2aaf0-109">1:</span><span class="sxs-lookup"><span data-stu-id="2aaf0-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="2aaf0-110">Crea una copia di backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="2aaf0-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="2aaf0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2aaf0-111">PARAMETERS</span></span>

### <span data-ttu-id="2aaf0-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="2aaf0-112">-BackupName</span></span>
<span data-ttu-id="2aaf0-113">Nome del backup</span><span class="sxs-lookup"><span data-stu-id="2aaf0-113">Backup Name</span></span>

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

### <span data-ttu-id="2aaf0-114">-Database</span><span class="sxs-lookup"><span data-stu-id="2aaf0-114">-Databases</span></span>
<span data-ttu-id="2aaf0-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="2aaf0-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="2aaf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf0-116">-DefaultProfile</span></span>
<span data-ttu-id="2aaf0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aaf0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2aaf0-118">-Name</span></span>
<span data-ttu-id="2aaf0-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="2aaf0-119">WebApp Name</span></span>

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

### <span data-ttu-id="2aaf0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf0-120">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf0-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2aaf0-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2aaf0-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="2aaf0-122">-Slot</span></span>
<span data-ttu-id="2aaf0-123">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="2aaf0-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2aaf0-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="2aaf0-124">-StorageAccountUrl</span></span>
<span data-ttu-id="2aaf0-125">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2aaf0-125">Storage Account Url</span></span>

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

### <span data-ttu-id="2aaf0-126">-Web App</span><span class="sxs-lookup"><span data-stu-id="2aaf0-126">-WebApp</span></span>
<span data-ttu-id="2aaf0-127">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="2aaf0-127">WebApp Object</span></span>

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

### <span data-ttu-id="2aaf0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf0-128">CommonParameters</span></span>
<span data-ttu-id="2aaf0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf0-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aaf0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2aaf0-131">INPUTS</span></span>

### <span data-ttu-id="2aaf0-132">Sito</span><span class="sxs-lookup"><span data-stu-id="2aaf0-132">Site</span></span>
<span data-ttu-id="2aaf0-133">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2aaf0-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2aaf0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aaf0-134">OUTPUTS</span></span>

### <span data-ttu-id="2aaf0-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="2aaf0-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="2aaf0-136">Note</span><span class="sxs-lookup"><span data-stu-id="2aaf0-136">NOTES</span></span>

## <span data-ttu-id="2aaf0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aaf0-137">RELATED LINKS</span></span>

