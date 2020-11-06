---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517935"
---
# <span data-ttu-id="0c23e-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0c23e-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="0c23e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c23e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c23e-103">Ottiene le informazioni sull'operazione per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="0c23e-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c23e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c23e-104">SYNTAX</span></span>

### <span data-ttu-id="0c23e-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c23e-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c23e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0c23e-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c23e-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="0c23e-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c23e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c23e-108">DESCRIPTION</span></span>
<span data-ttu-id="0c23e-109">Il cmdlet **Get-AzureRmSiteRecoveryJob** ottiene i processi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c23e-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="0c23e-110">Puoi usare questo cmdlet per visualizzare le informazioni sull'operazione per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="0c23e-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="0c23e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c23e-111">EXAMPLES</span></span>

## <span data-ttu-id="0c23e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c23e-112">PARAMETERS</span></span>

### <span data-ttu-id="0c23e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c23e-113">-DefaultProfile</span></span>
<span data-ttu-id="0c23e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c23e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c23e-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0c23e-115">-EndTime</span></span>
<span data-ttu-id="0c23e-116">Specifica l'ora di fine per i processi.</span><span class="sxs-lookup"><span data-stu-id="0c23e-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="0c23e-117">Questo cmdlet ottiene tutti i processi avviati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="0c23e-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="0c23e-118">Per ottenere un oggetto **DateTime** per questo parametro, usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0c23e-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="0c23e-119">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0c23e-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0c23e-120">-Job</span><span class="sxs-lookup"><span data-stu-id="0c23e-120">-Job</span></span>
<span data-ttu-id="0c23e-121">Specifica il processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0c23e-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="0c23e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c23e-122">-Name</span></span>
<span data-ttu-id="0c23e-123">Specifica un nome univoco che identifica il processo.</span><span class="sxs-lookup"><span data-stu-id="0c23e-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="0c23e-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0c23e-124">-StartTime</span></span>
<span data-ttu-id="0c23e-125">Specifica l'ora di inizio per i processi.</span><span class="sxs-lookup"><span data-stu-id="0c23e-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="0c23e-126">Questo cmdlet ottiene tutti i processi avviati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="0c23e-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="0c23e-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="0c23e-127">-State</span></span>
<span data-ttu-id="0c23e-128">Specifica lo stato di input per un processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0c23e-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="0c23e-129">Questo cmdlet ottiene tutti i processi che corrispondono allo stato specificato.</span><span class="sxs-lookup"><span data-stu-id="0c23e-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="0c23e-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c23e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c23e-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="0c23e-131">NotStarted</span></span>
- <span data-ttu-id="0c23e-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="0c23e-132">InProgress</span></span>
- <span data-ttu-id="0c23e-133">Succeeded</span><span class="sxs-lookup"><span data-stu-id="0c23e-133">Succeeded</span></span>
- <span data-ttu-id="0c23e-134">Altri</span><span class="sxs-lookup"><span data-stu-id="0c23e-134">Other</span></span>
- <span data-ttu-id="0c23e-135">Fallito</span><span class="sxs-lookup"><span data-stu-id="0c23e-135">Failed</span></span>
- <span data-ttu-id="0c23e-136">Annullata</span><span class="sxs-lookup"><span data-stu-id="0c23e-136">Cancelled</span></span>
- <span data-ttu-id="0c23e-137">Sospeso</span><span class="sxs-lookup"><span data-stu-id="0c23e-137">Suspended</span></span>

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

### <span data-ttu-id="0c23e-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="0c23e-138">-TargetObjectId</span></span>
<span data-ttu-id="0c23e-139">Specifica l'ID dell'oggetto di destinazione del processo.</span><span class="sxs-lookup"><span data-stu-id="0c23e-139">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="0c23e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c23e-140">CommonParameters</span></span>
<span data-ttu-id="0c23e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c23e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c23e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c23e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c23e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c23e-143">INPUTS</span></span>

### <span data-ttu-id="0c23e-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="0c23e-144">ASRJob</span></span>
<span data-ttu-id="0c23e-145">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0c23e-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="0c23e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c23e-146">OUTPUTS</span></span>

### <span data-ttu-id="0c23e-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="0c23e-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="0c23e-148">Note</span><span class="sxs-lookup"><span data-stu-id="0c23e-148">NOTES</span></span>

## <span data-ttu-id="0c23e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c23e-149">RELATED LINKS</span></span>

[<span data-ttu-id="0c23e-150">Riavviare-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0c23e-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="0c23e-151">Curriculum vitae-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0c23e-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="0c23e-152">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0c23e-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
