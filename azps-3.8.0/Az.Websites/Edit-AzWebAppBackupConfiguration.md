---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019635"
---
# <span data-ttu-id="5807f-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5807f-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5807f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5807f-102">SYNOPSIS</span></span>

## <span data-ttu-id="5807f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5807f-103">SYNTAX</span></span>

### <span data-ttu-id="5807f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5807f-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="5807f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5807f-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="5807f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5807f-106">DESCRIPTION</span></span>
<span data-ttu-id="5807f-107">Il cmdlet **Edit-AzWebAppBackupConfiguration** modifica il backup corrente della configurazione per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="5807f-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="5807f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5807f-108">EXAMPLES</span></span>

## <span data-ttu-id="5807f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5807f-109">PARAMETERS</span></span>

### <span data-ttu-id="5807f-110">-Database</span><span class="sxs-lookup"><span data-stu-id="5807f-110">-Databases</span></span>
<span data-ttu-id="5807f-111">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="5807f-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5807f-112">-DefaultProfile</span></span>
<span data-ttu-id="5807f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5807f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5807f-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="5807f-114">-FrequencyInterval</span></span>
<span data-ttu-id="5807f-115">Intervallo di frequenza</span><span class="sxs-lookup"><span data-stu-id="5807f-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="5807f-116">-FrequencyUnit</span></span>
<span data-ttu-id="5807f-117">Unità di frequenza</span><span class="sxs-lookup"><span data-stu-id="5807f-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="5807f-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="5807f-119">Mantieni almeno un'opzione di backup</span><span class="sxs-lookup"><span data-stu-id="5807f-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5807f-120">-Name</span></span>
<span data-ttu-id="5807f-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="5807f-121">WebApp Name</span></span>

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

### <span data-ttu-id="5807f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5807f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5807f-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5807f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5807f-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5807f-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="5807f-125">Periodo di conservazione in giorni</span><span class="sxs-lookup"><span data-stu-id="5807f-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="5807f-126">-Slot</span></span>
<span data-ttu-id="5807f-127">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="5807f-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5807f-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5807f-128">-StartTime</span></span>
<span data-ttu-id="5807f-129">StartTime in formato UTC</span><span class="sxs-lookup"><span data-stu-id="5807f-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="5807f-130">-StorageAccountUrl</span></span>
<span data-ttu-id="5807f-131">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5807f-131">Storage Account Url</span></span>

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

### <span data-ttu-id="5807f-132">-Web App</span><span class="sxs-lookup"><span data-stu-id="5807f-132">-WebApp</span></span>
<span data-ttu-id="5807f-133">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="5807f-133">WebApp Object</span></span>

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

### <span data-ttu-id="5807f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5807f-134">CommonParameters</span></span>
<span data-ttu-id="5807f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5807f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5807f-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5807f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5807f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5807f-137">INPUTS</span></span>

### <span data-ttu-id="5807f-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5807f-138">System.Int32</span></span>

### <span data-ttu-id="5807f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5807f-139">System.String</span></span>

### <span data-ttu-id="5807f-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5807f-140">System.DateTime</span></span>

### <span data-ttu-id="5807f-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5807f-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5807f-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5807f-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="5807f-143">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="5807f-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="5807f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5807f-144">OUTPUTS</span></span>

### <span data-ttu-id="5807f-145">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5807f-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5807f-146">Note</span><span class="sxs-lookup"><span data-stu-id="5807f-146">NOTES</span></span>

## <span data-ttu-id="5807f-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5807f-147">RELATED LINKS</span></span>

[<span data-ttu-id="5807f-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5807f-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


