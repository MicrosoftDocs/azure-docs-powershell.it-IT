---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512788"
---
# <span data-ttu-id="f8c8b-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c8b-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f8c8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8c8b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8c8b-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8c8b-103">SYNTAX</span></span>

### <span data-ttu-id="f8c8b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f8c8b-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f8c8b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f8c8b-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f8c8b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8c8b-106">DESCRIPTION</span></span>
<span data-ttu-id="f8c8b-107">Il cmdlet **Edit-AzureRmWebAppBackupConfiguration** modifica il backup corrente della configurazione per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="f8c8b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8c8b-108">EXAMPLES</span></span>

## <span data-ttu-id="f8c8b-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8c8b-109">PARAMETERS</span></span>

### <span data-ttu-id="f8c8b-110">-Database</span><span class="sxs-lookup"><span data-stu-id="f8c8b-110">-Databases</span></span>
<span data-ttu-id="f8c8b-111">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f8c8b-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f8c8b-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="f8c8b-112">-FrequencyInterval</span></span>
<span data-ttu-id="f8c8b-113">Intervallo di frequenza</span><span class="sxs-lookup"><span data-stu-id="f8c8b-113">Frequency Interval</span></span>

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

### <span data-ttu-id="f8c8b-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="f8c8b-114">-FrequencyUnit</span></span>
<span data-ttu-id="f8c8b-115">Unità di frequenza</span><span class="sxs-lookup"><span data-stu-id="f8c8b-115">Frequency Unit</span></span>

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

### <span data-ttu-id="f8c8b-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="f8c8b-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="f8c8b-117">Mantieni almeno un'opzione di backup</span><span class="sxs-lookup"><span data-stu-id="f8c8b-117">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="f8c8b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8c8b-118">-Name</span></span>
<span data-ttu-id="f8c8b-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="f8c8b-119">WebApp Name</span></span>

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

### <span data-ttu-id="f8c8b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c8b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8c8b-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f8c8b-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f8c8b-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f8c8b-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f8c8b-123">Periodo di conservazione in giorni</span><span class="sxs-lookup"><span data-stu-id="f8c8b-123">Retention Period In Days</span></span>

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

### <span data-ttu-id="f8c8b-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="f8c8b-124">-Slot</span></span>
<span data-ttu-id="f8c8b-125">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="f8c8b-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f8c8b-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f8c8b-126">-StartTime</span></span>
<span data-ttu-id="f8c8b-127">StartTime in formato UTC</span><span class="sxs-lookup"><span data-stu-id="f8c8b-127">StartTime in UTC</span></span>

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

### <span data-ttu-id="f8c8b-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f8c8b-128">-StorageAccountUrl</span></span>
<span data-ttu-id="f8c8b-129">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f8c8b-129">Storage Account Url</span></span>

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

### <span data-ttu-id="f8c8b-130">-Web App</span><span class="sxs-lookup"><span data-stu-id="f8c8b-130">-WebApp</span></span>
<span data-ttu-id="f8c8b-131">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="f8c8b-131">WebApp Object</span></span>

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

### <span data-ttu-id="f8c8b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c8b-132">-DefaultProfile</span></span>
<span data-ttu-id="f8c8b-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c8b-134">CommonParameters</span></span>
<span data-ttu-id="f8c8b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c8b-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c8b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c8b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8c8b-137">INPUTS</span></span>

### <span data-ttu-id="f8c8b-138">Sito</span><span class="sxs-lookup"><span data-stu-id="f8c8b-138">Site</span></span>
<span data-ttu-id="f8c8b-139">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8c8b-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f8c8b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8c8b-140">OUTPUTS</span></span>

### <span data-ttu-id="f8c8b-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c8b-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f8c8b-142">Note</span><span class="sxs-lookup"><span data-stu-id="f8c8b-142">NOTES</span></span>

## <span data-ttu-id="f8c8b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8c8b-143">RELATED LINKS</span></span>

[<span data-ttu-id="f8c8b-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c8b-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


