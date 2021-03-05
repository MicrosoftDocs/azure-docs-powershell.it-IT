---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996699"
---
# <span data-ttu-id="afef1-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="afef1-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="afef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afef1-102">SYNOPSIS</span></span>
<span data-ttu-id="afef1-103">Crea l'impostazione di sincronizzazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="afef1-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="afef1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afef1-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afef1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="afef1-105">DESCRIPTION</span></span>
<span data-ttu-id="afef1-106">**New-AzDataShareSynchronizationSetting** crea un'impostazione di sincronizzazione per la condivisione nell'account di condivisione per un intervallo di ricorrenza giornaliero o orario in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="afef1-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="afef1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afef1-107">EXAMPLES</span></span>

### <span data-ttu-id="afef1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afef1-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="afef1-109">Questo comando crea un'impostazione di sincronizzazione nell'intervallo di ricorrenza giornaliera alle 9:00 per condividere AdsShare nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="afef1-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="afef1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afef1-110">PARAMETERS</span></span>

### <span data-ttu-id="afef1-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afef1-111">-AccountName</span></span>
<span data-ttu-id="afef1-112">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="afef1-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afef1-113">-DefaultProfile</span></span>
<span data-ttu-id="afef1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afef1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afef1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="afef1-115">-Name</span></span>
<span data-ttu-id="afef1-116">Nome dell'impostazione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="afef1-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="afef1-117">-RecurrenceInterval</span></span>
<span data-ttu-id="afef1-118">Intervallo di ricorrenza per l'impostazione di sincronizzazione (giorno o ora)</span><span class="sxs-lookup"><span data-stu-id="afef1-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afef1-119">-ResourceGroupName</span></span>
<span data-ttu-id="afef1-120">Nome del gruppo di risorse dell'account azure data share</span><span class="sxs-lookup"><span data-stu-id="afef1-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="afef1-121">-ShareName</span></span>
<span data-ttu-id="afef1-122">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="afef1-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="afef1-123">-SynchronizationTime</span></span>
<span data-ttu-id="afef1-124">Ora di inizio dell'impostazione di sincronizzazione pianificata</span><span class="sxs-lookup"><span data-stu-id="afef1-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afef1-125">-Confirm</span></span>
<span data-ttu-id="afef1-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afef1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afef1-127">-WhatIf</span></span>
<span data-ttu-id="afef1-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afef1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afef1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afef1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afef1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afef1-130">CommonParameters</span></span>
<span data-ttu-id="afef1-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afef1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afef1-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="afef1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afef1-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="afef1-133">INPUTS</span></span>

### <span data-ttu-id="afef1-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="afef1-134">None</span></span>

## <span data-ttu-id="afef1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afef1-135">OUTPUTS</span></span>

### <span data-ttu-id="afef1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="afef1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="afef1-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="afef1-137">NOTES</span></span>

## <span data-ttu-id="afef1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afef1-138">RELATED LINKS</span></span>
