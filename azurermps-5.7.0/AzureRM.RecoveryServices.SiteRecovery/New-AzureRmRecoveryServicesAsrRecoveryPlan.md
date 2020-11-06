---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512400"
---
# <span data-ttu-id="d74d4-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d74d4-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d74d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d74d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d74d4-103">Crea un piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="d74d4-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d74d4-104">SYNTAX</span></span>

### <span data-ttu-id="d74d4-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d74d4-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74d4-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d74d4-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74d4-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="d74d4-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d74d4-108">DESCRIPTION</span></span>
<span data-ttu-id="d74d4-109">Il cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** crea un piano di ripristino di un sito di Azure nel Vault di Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d74d4-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="d74d4-110">Un piano di ripristino raccoglie le macchine virtuali appartenenti a un'applicazione in un'unità per consentire loro di essere recuperate insieme.</span><span class="sxs-lookup"><span data-stu-id="d74d4-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="d74d4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d74d4-111">EXAMPLES</span></span>

### <span data-ttu-id="d74d4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d74d4-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="d74d4-113">Avvia l'operazione di creazione del piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d74d4-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d74d4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d74d4-114">PARAMETERS</span></span>

### <span data-ttu-id="d74d4-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="d74d4-115">-Azure</span></span>
<span data-ttu-id="d74d4-116">Parametro switch per specificare che la posizione di ripristino per il piano di ripristino è Azure.</span><span class="sxs-lookup"><span data-stu-id="d74d4-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d74d4-117">-Confirm</span></span>
<span data-ttu-id="d74d4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74d4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74d4-119">-DefaultProfile</span></span>
<span data-ttu-id="d74d4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d74d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d74d4-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="d74d4-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="d74d4-122">Specifica il modello di distribuzione di failover (Classic o Resource Manager) degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d74d4-123">-Name</span></span>
<span data-ttu-id="d74d4-124">Nome del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-124">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-125">-Path</span><span class="sxs-lookup"><span data-stu-id="d74d4-125">-Path</span></span>
<span data-ttu-id="d74d4-126">Specifica il percorso del file JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="d74d4-127">Per creare il piano di ripristino, è possibile usare un JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="d74d4-128">-PrimaryFabric</span></span>
<span data-ttu-id="d74d4-129">Specifica l'oggetto del tessuto ASR per il tessuto ASR principale degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d74d4-130">-RecoveryFabric</span></span>
<span data-ttu-id="d74d4-131">Specifica l'oggetto del tessuto ASR per il tessuto ASR di ripristino degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-132">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d74d4-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d74d4-133">Elenco di elementi protetti per la replica da aggiungere al primo gruppo del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d74d4-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74d4-134">-WhatIf</span></span>
<span data-ttu-id="d74d4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d74d4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d74d4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d74d4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74d4-137">CommonParameters</span></span>
<span data-ttu-id="d74d4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74d4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d74d4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74d4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d74d4-140">INPUTS</span></span>

### <span data-ttu-id="d74d4-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="d74d4-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="d74d4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d74d4-142">OUTPUTS</span></span>

### <span data-ttu-id="d74d4-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="d74d4-143">System.Object</span></span>

## <span data-ttu-id="d74d4-144">Note</span><span class="sxs-lookup"><span data-stu-id="d74d4-144">NOTES</span></span>

## <span data-ttu-id="d74d4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d74d4-145">RELATED LINKS</span></span>

[<span data-ttu-id="d74d4-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d74d4-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d74d4-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d74d4-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d74d4-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d74d4-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


