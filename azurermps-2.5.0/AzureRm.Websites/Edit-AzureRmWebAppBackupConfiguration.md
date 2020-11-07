---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 9a90e56909de016bb388be1a43f5b41c8e47e9e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865999"
---
# <span data-ttu-id="b5112-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5112-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="b5112-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5112-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5112-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5112-103">SYNTAX</span></span>

### <span data-ttu-id="b5112-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b5112-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="b5112-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b5112-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="b5112-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5112-106">DESCRIPTION</span></span>
<span data-ttu-id="b5112-107">Il cmdlet **Edit-AzureRmWebAppBackupConfiguration** modifica il backup corrente della configurazione per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="b5112-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="b5112-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5112-108">EXAMPLES</span></span>

## <span data-ttu-id="b5112-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5112-109">PARAMETERS</span></span>

### <span data-ttu-id="b5112-110">-Database</span><span class="sxs-lookup"><span data-stu-id="b5112-110">-Databases</span></span>
<span data-ttu-id="b5112-111">Database di tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="b5112-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="b5112-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5112-112">-DefaultProfile</span></span>
<span data-ttu-id="b5112-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5112-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5112-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="b5112-114">-FrequencyInterval</span></span>
<span data-ttu-id="b5112-115">Intervallo di frequenza</span><span class="sxs-lookup"><span data-stu-id="b5112-115">Frequency Interval</span></span>

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

### <span data-ttu-id="b5112-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="b5112-116">-FrequencyUnit</span></span>
<span data-ttu-id="b5112-117">Unità di frequenza</span><span class="sxs-lookup"><span data-stu-id="b5112-117">Frequency Unit</span></span>

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

### <span data-ttu-id="b5112-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="b5112-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="b5112-119">Mantieni almeno un'opzione di backup</span><span class="sxs-lookup"><span data-stu-id="b5112-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="b5112-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5112-120">-Name</span></span>
<span data-ttu-id="b5112-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b5112-121">WebApp Name</span></span>

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

### <span data-ttu-id="b5112-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5112-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5112-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b5112-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b5112-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b5112-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="b5112-125">Periodo di conservazione in giorni</span><span class="sxs-lookup"><span data-stu-id="b5112-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="b5112-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5112-126">-Slot</span></span>
<span data-ttu-id="b5112-127">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="b5112-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b5112-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5112-128">-StartTime</span></span>
<span data-ttu-id="b5112-129">StartTime in formato UTC</span><span class="sxs-lookup"><span data-stu-id="b5112-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="b5112-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b5112-130">-StorageAccountUrl</span></span>
<span data-ttu-id="b5112-131">URL dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b5112-131">Storage Account Url</span></span>

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

### <span data-ttu-id="b5112-132">-Web App</span><span class="sxs-lookup"><span data-stu-id="b5112-132">-WebApp</span></span>
<span data-ttu-id="b5112-133">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="b5112-133">WebApp Object</span></span>

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

### <span data-ttu-id="b5112-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5112-134">CommonParameters</span></span>
<span data-ttu-id="b5112-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5112-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5112-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5112-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5112-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5112-137">INPUTS</span></span>

### <span data-ttu-id="b5112-138">Sito</span><span class="sxs-lookup"><span data-stu-id="b5112-138">Site</span></span>
<span data-ttu-id="b5112-139">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b5112-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b5112-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5112-140">OUTPUTS</span></span>

### <span data-ttu-id="b5112-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5112-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="b5112-142">Note</span><span class="sxs-lookup"><span data-stu-id="b5112-142">NOTES</span></span>

## <span data-ttu-id="b5112-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5112-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5112-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5112-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


