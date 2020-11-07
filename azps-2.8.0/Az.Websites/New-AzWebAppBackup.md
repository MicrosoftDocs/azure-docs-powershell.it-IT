---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858569"
---
# <span data-ttu-id="34c95-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="34c95-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="34c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34c95-102">SYNOPSIS</span></span>

## <span data-ttu-id="34c95-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34c95-103">SYNTAX</span></span>

### <span data-ttu-id="34c95-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="34c95-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="34c95-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="34c95-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="34c95-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34c95-106">DESCRIPTION</span></span>
<span data-ttu-id="34c95-107">Il cmdlet **New-AzWebAppBackup** crea un backup di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="34c95-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="34c95-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34c95-108">EXAMPLES</span></span>

### <span data-ttu-id="34c95-109">1:</span><span class="sxs-lookup"><span data-stu-id="34c95-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="34c95-110">Crea una copia di backup dell'app specificata ContosoWebApp che si trova all'interno di un gruppo di risorse predefinito-Web-Westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="34c95-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="34c95-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34c95-111">PARAMETERS</span></span>

### <span data-ttu-id="34c95-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="34c95-112">-BackupName</span></span>
<span data-ttu-id="34c95-113">Nome del backup</span><span class="sxs-lookup"><span data-stu-id="34c95-113">Backup Name</span></span>

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

### <span data-ttu-id="34c95-114">-Database</span><span class="sxs-lookup"><span data-stu-id="34c95-114">-Databases</span></span>
<span data-ttu-id="34c95-115">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="34c95-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="34c95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c95-116">-DefaultProfile</span></span>
<span data-ttu-id="34c95-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34c95-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c95-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="34c95-118">-Name</span></span>
<span data-ttu-id="34c95-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="34c95-119">WebApp Name</span></span>

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

### <span data-ttu-id="34c95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c95-120">-ResourceGroupName</span></span>
<span data-ttu-id="34c95-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="34c95-121">Resource Group Name</span></span>

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

### <span data-ttu-id="34c95-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="34c95-122">-Slot</span></span>
<span data-ttu-id="34c95-123">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="34c95-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="34c95-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="34c95-124">-StorageAccountUrl</span></span>
<span data-ttu-id="34c95-125">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="34c95-125">Storage Account Url</span></span>

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

### <span data-ttu-id="34c95-126">-Web App</span><span class="sxs-lookup"><span data-stu-id="34c95-126">-WebApp</span></span>
<span data-ttu-id="34c95-127">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="34c95-127">WebApp Object</span></span>

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

### <span data-ttu-id="34c95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c95-128">CommonParameters</span></span>
<span data-ttu-id="34c95-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c95-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c95-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c95-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34c95-131">INPUTS</span></span>

### <span data-ttu-id="34c95-132">System. String</span><span class="sxs-lookup"><span data-stu-id="34c95-132">System.String</span></span>

### <span data-ttu-id="34c95-133">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="34c95-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="34c95-134">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="34c95-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="34c95-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34c95-135">OUTPUTS</span></span>

### <span data-ttu-id="34c95-136">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="34c95-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="34c95-137">Note</span><span class="sxs-lookup"><span data-stu-id="34c95-137">NOTES</span></span>

## <span data-ttu-id="34c95-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34c95-138">RELATED LINKS</span></span>
