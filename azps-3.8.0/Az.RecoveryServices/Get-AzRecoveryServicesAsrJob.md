---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864288"
---
# <span data-ttu-id="4ec53-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="4ec53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ec53-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec53-103">Ottiene i dettagli del processo ASR specificato o l'elenco dei processi ASR recenti nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4ec53-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="4ec53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ec53-104">SYNTAX</span></span>

### <span data-ttu-id="4ec53-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ec53-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec53-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4ec53-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec53-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="4ec53-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec53-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ec53-108">DESCRIPTION</span></span>
<span data-ttu-id="4ec53-109">Il cmdlet **Get-AzRecoveryServicesAsrJob** ottiene i processi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec53-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="4ec53-110">Puoi usare questo cmdlet per visualizzare i processi ASR nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4ec53-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="4ec53-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ec53-111">EXAMPLES</span></span>

### <span data-ttu-id="4ec53-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ec53-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="4ec53-113">Restituisce tutti i processi su un determinato oggetto ASR (fare riferimento all'oggetto ASR, ad esempio elemento replicato o piano di ripristino, in base all'ID.)</span><span class="sxs-lookup"><span data-stu-id="4ec53-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="4ec53-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ec53-114">PARAMETERS</span></span>

### <span data-ttu-id="4ec53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec53-115">-DefaultProfile</span></span>
<span data-ttu-id="4ec53-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4ec53-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4ec53-117">-EndTime</span></span>
<span data-ttu-id="4ec53-118">Specifica l'ora di fine per i processi.</span><span class="sxs-lookup"><span data-stu-id="4ec53-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="4ec53-119">Questo cmdlet ottiene tutti i processi avviati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec53-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="4ec53-120">Per ottenere un oggetto **DateTime** per questo parametro, usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4ec53-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4ec53-121">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4ec53-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-122">-Job</span><span class="sxs-lookup"><span data-stu-id="4ec53-122">-Job</span></span>
<span data-ttu-id="4ec53-123">Specifica l'oggetto processo ASR per cui ottenere i dettagli aggiornati.</span><span class="sxs-lookup"><span data-stu-id="4ec53-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ec53-124">-Name</span></span>
<span data-ttu-id="4ec53-125">Specificare il processo ASR per nome.</span><span class="sxs-lookup"><span data-stu-id="4ec53-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4ec53-126">-StartTime</span></span>
<span data-ttu-id="4ec53-127">Specifica l'ora di inizio per i processi.</span><span class="sxs-lookup"><span data-stu-id="4ec53-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="4ec53-128">Questo cmdlet ottiene tutti i processi avviati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec53-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="4ec53-129">-State</span></span>
<span data-ttu-id="4ec53-130">Specifica lo stato per un processo ASR.</span><span class="sxs-lookup"><span data-stu-id="4ec53-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="4ec53-131">Questo cmdlet ottiene tutti i processi che corrispondono allo stato specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec53-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="4ec53-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ec53-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ec53-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="4ec53-133">NotStarted</span></span>
- <span data-ttu-id="4ec53-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="4ec53-134">InProgress</span></span>
- <span data-ttu-id="4ec53-135">Succeeded</span><span class="sxs-lookup"><span data-stu-id="4ec53-135">Succeeded</span></span>
- <span data-ttu-id="4ec53-136">Altri</span><span class="sxs-lookup"><span data-stu-id="4ec53-136">Other</span></span>
- <span data-ttu-id="4ec53-137">Fallito</span><span class="sxs-lookup"><span data-stu-id="4ec53-137">Failed</span></span>
- <span data-ttu-id="4ec53-138">Annullata</span><span class="sxs-lookup"><span data-stu-id="4ec53-138">Cancelled</span></span>
- <span data-ttu-id="4ec53-139">Sospeso</span><span class="sxs-lookup"><span data-stu-id="4ec53-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="4ec53-140">-TargetObjectId</span></span>
<span data-ttu-id="4ec53-141">Specifica l'ID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ec53-141">Specifies the ID of the object.</span></span> <span data-ttu-id="4ec53-142">Usato per cercare processi nell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="4ec53-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec53-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec53-143">CommonParameters</span></span>
<span data-ttu-id="4ec53-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec53-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec53-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ec53-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec53-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ec53-146">INPUTS</span></span>

### <span data-ttu-id="4ec53-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ec53-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ec53-148">OUTPUTS</span></span>

### <span data-ttu-id="4ec53-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ec53-150">Note</span><span class="sxs-lookup"><span data-stu-id="4ec53-150">NOTES</span></span>

## <span data-ttu-id="4ec53-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ec53-151">RELATED LINKS</span></span>

[<span data-ttu-id="4ec53-152">Riavviare-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="4ec53-153">Curriculum vitae-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="4ec53-154">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4ec53-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
