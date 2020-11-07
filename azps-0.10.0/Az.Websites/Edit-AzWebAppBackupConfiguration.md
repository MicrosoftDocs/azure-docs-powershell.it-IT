---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861973"
---
# <span data-ttu-id="e4383-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4383-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="e4383-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4383-102">SYNOPSIS</span></span>

## <span data-ttu-id="e4383-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4383-103">SYNTAX</span></span>

### <span data-ttu-id="e4383-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e4383-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="e4383-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e4383-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="e4383-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4383-106">DESCRIPTION</span></span>
<span data-ttu-id="e4383-107">Il cmdlet **Edit-AzWebAppBackupConfiguration** modifica il backup corrente della configurazione per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="e4383-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="e4383-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4383-108">EXAMPLES</span></span>

## <span data-ttu-id="e4383-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4383-109">PARAMETERS</span></span>

### <span data-ttu-id="e4383-110">-Database</span><span class="sxs-lookup"><span data-stu-id="e4383-110">-Databases</span></span>
<span data-ttu-id="e4383-111">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="e4383-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4383-112">-DefaultProfile</span></span>
<span data-ttu-id="e4383-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4383-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4383-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="e4383-114">-FrequencyInterval</span></span>
<span data-ttu-id="e4383-115">Intervallo di frequenza</span><span class="sxs-lookup"><span data-stu-id="e4383-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="e4383-116">-FrequencyUnit</span></span>
<span data-ttu-id="e4383-117">Unità di frequenza</span><span class="sxs-lookup"><span data-stu-id="e4383-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="e4383-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="e4383-119">Mantieni almeno un'opzione di backup</span><span class="sxs-lookup"><span data-stu-id="e4383-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4383-120">-Name</span></span>
<span data-ttu-id="e4383-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e4383-121">WebApp Name</span></span>

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

### <span data-ttu-id="e4383-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4383-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4383-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e4383-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e4383-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="e4383-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="e4383-125">Periodo di conservazione in giorni</span><span class="sxs-lookup"><span data-stu-id="e4383-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="e4383-126">-Slot</span></span>
<span data-ttu-id="e4383-127">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="e4383-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e4383-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e4383-128">-StartTime</span></span>
<span data-ttu-id="e4383-129">StartTime in formato UTC</span><span class="sxs-lookup"><span data-stu-id="e4383-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4383-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e4383-130">-StorageAccountUrl</span></span>
<span data-ttu-id="e4383-131">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e4383-131">Storage Account Url</span></span>

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

### <span data-ttu-id="e4383-132">-Web App</span><span class="sxs-lookup"><span data-stu-id="e4383-132">-WebApp</span></span>
<span data-ttu-id="e4383-133">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="e4383-133">WebApp Object</span></span>

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

### <span data-ttu-id="e4383-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4383-134">CommonParameters</span></span>
<span data-ttu-id="e4383-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4383-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4383-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4383-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4383-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4383-137">INPUTS</span></span>

### <span data-ttu-id="e4383-138">Sito</span><span class="sxs-lookup"><span data-stu-id="e4383-138">Site</span></span>
<span data-ttu-id="e4383-139">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e4383-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e4383-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4383-140">OUTPUTS</span></span>

### <span data-ttu-id="e4383-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4383-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="e4383-142">Note</span><span class="sxs-lookup"><span data-stu-id="e4383-142">NOTES</span></span>

## <span data-ttu-id="e4383-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4383-143">RELATED LINKS</span></span>

[<span data-ttu-id="e4383-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4383-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


