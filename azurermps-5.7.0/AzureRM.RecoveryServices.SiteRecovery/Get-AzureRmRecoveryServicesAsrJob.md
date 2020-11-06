---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509695"
---
# <span data-ttu-id="9b7b8-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7b8-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9b7b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7b8-103">Ottiene i dettagli del processo ASR specificato o l'elenco dei processi ASR recenti nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b7b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-104">SYNTAX</span></span>

### <span data-ttu-id="9b7b8-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b7b8-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b7b8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9b7b8-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b7b8-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="9b7b8-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b7b8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7b8-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrJob** ottiene i processi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="9b7b8-110">Puoi usare questo cmdlet per visualizzare i processi ASR nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="9b7b8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-111">EXAMPLES</span></span>

### <span data-ttu-id="9b7b8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b7b8-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="9b7b8-113">Restituisce tutti i processi su un determinato oggetto ASR (fare riferimento all'oggetto ASR, ad esempio elemento replicato o piano di ripristino, in base all'ID.)</span><span class="sxs-lookup"><span data-stu-id="9b7b8-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="9b7b8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-114">PARAMETERS</span></span>

### <span data-ttu-id="9b7b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7b8-115">-DefaultProfile</span></span>
<span data-ttu-id="9b7b8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="9b7b8-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9b7b8-117">-EndTime</span></span>
<span data-ttu-id="9b7b8-118">Specifica l'ora di fine per i processi.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="9b7b8-119">Questo cmdlet ottiene tutti i processi avviati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="9b7b8-120">Per ottenere un oggetto **DateTime** per questo parametro, usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9b7b8-121">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9b7b8-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-122">-Job</span><span class="sxs-lookup"><span data-stu-id="9b7b8-122">-Job</span></span>
<span data-ttu-id="9b7b8-123">Specifica l'oggetto processo ASR per cui ottenere i dettagli aggiornati.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b7b8-124">-Name</span></span>
<span data-ttu-id="9b7b8-125">Specificare il processo ASR per nome.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-125">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9b7b8-126">-StartTime</span></span>
<span data-ttu-id="9b7b8-127">Specifica l'ora di inizio per i processi.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="9b7b8-128">Questo cmdlet ottiene tutti i processi avviati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="9b7b8-129">-State</span></span>
<span data-ttu-id="9b7b8-130">Specifica lo stato per un processo ASR.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="9b7b8-131">Questo cmdlet ottiene tutti i processi che corrispondono allo stato specificato.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="9b7b8-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b7b8-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b7b8-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="9b7b8-133">NotStarted</span></span>
- <span data-ttu-id="9b7b8-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="9b7b8-134">InProgress</span></span>
- <span data-ttu-id="9b7b8-135">Succeeded</span><span class="sxs-lookup"><span data-stu-id="9b7b8-135">Succeeded</span></span>
- <span data-ttu-id="9b7b8-136">Altri</span><span class="sxs-lookup"><span data-stu-id="9b7b8-136">Other</span></span>
- <span data-ttu-id="9b7b8-137">Fallito</span><span class="sxs-lookup"><span data-stu-id="9b7b8-137">Failed</span></span>
- <span data-ttu-id="9b7b8-138">Annullata</span><span class="sxs-lookup"><span data-stu-id="9b7b8-138">Cancelled</span></span>
- <span data-ttu-id="9b7b8-139">Sospeso</span><span class="sxs-lookup"><span data-stu-id="9b7b8-139">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="9b7b8-140">-TargetObjectId</span></span>
<span data-ttu-id="9b7b8-141">Specifica l'ID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-141">Specifies the ID of the object.</span></span> <span data-ttu-id="9b7b8-142">Usato per cercare processi nell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7b8-143">CommonParameters</span></span>
<span data-ttu-id="9b7b8-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7b8-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7b8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7b8-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-146">INPUTS</span></span>

### <span data-ttu-id="9b7b8-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9b7b8-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b7b8-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b7b8-148">OUTPUTS</span></span>

### <span data-ttu-id="9b7b8-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9b7b8-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9b7b8-150">Note</span><span class="sxs-lookup"><span data-stu-id="9b7b8-150">NOTES</span></span>

## <span data-ttu-id="9b7b8-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-151">RELATED LINKS</span></span>

[<span data-ttu-id="9b7b8-152">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7b8-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b7b8-153">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7b8-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b7b8-154">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b7b8-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
