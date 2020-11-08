---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: d7f6429ebc3e8a3ebf1f8dd2749e6b7f66005ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019788"
---
# <span data-ttu-id="d4c89-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d4c89-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d4c89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4c89-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c89-103">Crea l'impostazione di sincronizzazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="d4c89-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="d4c89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4c89-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c89-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c89-106">Il **nuovo AzDataShareSynchronizationSetting** crea un'impostazione di sincronizzazione per la condivisione in un account di condivisione per un intervallo di ricorrenza giornaliero o ogni ora in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="d4c89-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="d4c89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4c89-107">EXAMPLES</span></span>

### <span data-ttu-id="d4c89-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4c89-108">Example 1</span></span>
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

<span data-ttu-id="d4c89-109">Questo comando crea un'impostazione di sincronizzazione nell'intervallo di ricorrenza giornaliera alle 9:00 AM per la condivisione di AdsShare in WikiAds dell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="d4c89-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="d4c89-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4c89-110">PARAMETERS</span></span>

### <span data-ttu-id="d4c89-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4c89-111">-AccountName</span></span>
<span data-ttu-id="d4c89-112">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d4c89-112">Azure data share account name</span></span>

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

### <span data-ttu-id="d4c89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c89-113">-DefaultProfile</span></span>
<span data-ttu-id="d4c89-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c89-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4c89-115">-Name</span></span>
<span data-ttu-id="d4c89-116">Nome impostazione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="d4c89-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="d4c89-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="d4c89-117">-RecurrenceInterval</span></span>
<span data-ttu-id="d4c89-118">Intervallo di ricorrenza per l'impostazione di sincronizzazione (giorno o ora)</span><span class="sxs-lookup"><span data-stu-id="d4c89-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="d4c89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c89-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4c89-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d4c89-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="d4c89-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d4c89-121">-ShareName</span></span>
<span data-ttu-id="d4c89-122">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d4c89-122">Azure data share name</span></span>

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

### <span data-ttu-id="d4c89-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="d4c89-123">-SynchronizationTime</span></span>
<span data-ttu-id="d4c89-124">Ora di inizio dell'impostazione di sincronizzazione pianificata</span><span class="sxs-lookup"><span data-stu-id="d4c89-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="d4c89-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4c89-125">-Confirm</span></span>
<span data-ttu-id="d4c89-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c89-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c89-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c89-127">-WhatIf</span></span>
<span data-ttu-id="d4c89-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4c89-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4c89-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4c89-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c89-130">CommonParameters</span></span>
<span data-ttu-id="d4c89-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c89-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c89-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c89-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4c89-133">INPUTS</span></span>

### <span data-ttu-id="d4c89-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d4c89-134">None</span></span>

## <span data-ttu-id="d4c89-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4c89-135">OUTPUTS</span></span>

### <span data-ttu-id="d4c89-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d4c89-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d4c89-137">Note</span><span class="sxs-lookup"><span data-stu-id="d4c89-137">NOTES</span></span>

## <span data-ttu-id="d4c89-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4c89-138">RELATED LINKS</span></span>
