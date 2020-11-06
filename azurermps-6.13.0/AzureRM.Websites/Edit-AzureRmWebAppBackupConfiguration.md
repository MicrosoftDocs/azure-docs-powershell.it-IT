---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: a7a66197752e7dd9ec58e7eeca921af277687ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508940"
---
# <span data-ttu-id="c9475-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9475-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c9475-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9475-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9475-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9475-103">SYNTAX</span></span>

### <span data-ttu-id="c9475-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c9475-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="c9475-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c9475-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="c9475-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9475-106">DESCRIPTION</span></span>
<span data-ttu-id="c9475-107">Il cmdlet **Edit-AzureRmWebAppBackupConfiguration** modifica il backup corrente della configurazione per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="c9475-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="c9475-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9475-108">EXAMPLES</span></span>

## <span data-ttu-id="c9475-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9475-109">PARAMETERS</span></span>

### <span data-ttu-id="c9475-110">-Database</span><span class="sxs-lookup"><span data-stu-id="c9475-110">-Databases</span></span>
<span data-ttu-id="c9475-111">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c9475-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="c9475-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9475-112">-DefaultProfile</span></span>
<span data-ttu-id="c9475-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9475-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9475-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="c9475-114">-FrequencyInterval</span></span>
<span data-ttu-id="c9475-115">Intervallo di frequenza</span><span class="sxs-lookup"><span data-stu-id="c9475-115">Frequency Interval</span></span>

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

### <span data-ttu-id="c9475-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="c9475-116">-FrequencyUnit</span></span>
<span data-ttu-id="c9475-117">Unità di frequenza</span><span class="sxs-lookup"><span data-stu-id="c9475-117">Frequency Unit</span></span>

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

### <span data-ttu-id="c9475-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="c9475-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="c9475-119">Mantieni almeno un'opzione di backup</span><span class="sxs-lookup"><span data-stu-id="c9475-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="c9475-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9475-120">-Name</span></span>
<span data-ttu-id="c9475-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="c9475-121">WebApp Name</span></span>

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

### <span data-ttu-id="c9475-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9475-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9475-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c9475-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c9475-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c9475-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c9475-125">Periodo di conservazione in giorni</span><span class="sxs-lookup"><span data-stu-id="c9475-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="c9475-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9475-126">-Slot</span></span>
<span data-ttu-id="c9475-127">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="c9475-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c9475-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c9475-128">-StartTime</span></span>
<span data-ttu-id="c9475-129">StartTime in formato UTC</span><span class="sxs-lookup"><span data-stu-id="c9475-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="c9475-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c9475-130">-StorageAccountUrl</span></span>
<span data-ttu-id="c9475-131">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c9475-131">Storage Account Url</span></span>

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

### <span data-ttu-id="c9475-132">-Web App</span><span class="sxs-lookup"><span data-stu-id="c9475-132">-WebApp</span></span>
<span data-ttu-id="c9475-133">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="c9475-133">WebApp Object</span></span>

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

### <span data-ttu-id="c9475-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9475-134">CommonParameters</span></span>
<span data-ttu-id="c9475-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9475-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9475-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9475-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9475-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9475-137">INPUTS</span></span>

### <span data-ttu-id="c9475-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c9475-138">System.Int32</span></span>

### <span data-ttu-id="c9475-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c9475-139">System.String</span></span>

### <span data-ttu-id="c9475-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c9475-140">System.DateTime</span></span>

### <span data-ttu-id="c9475-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9475-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c9475-142">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="c9475-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c9475-143">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9475-143">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="c9475-144">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c9475-144">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="c9475-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9475-145">OUTPUTS</span></span>

### <span data-ttu-id="c9475-146">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9475-146">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c9475-147">Note</span><span class="sxs-lookup"><span data-stu-id="c9475-147">NOTES</span></span>

## <span data-ttu-id="c9475-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9475-148">RELATED LINKS</span></span>

[<span data-ttu-id="c9475-149">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9475-149">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


