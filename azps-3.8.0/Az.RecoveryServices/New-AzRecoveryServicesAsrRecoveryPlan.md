---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022646"
---
# <span data-ttu-id="7f171-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f171-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7f171-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f171-102">SYNOPSIS</span></span>
<span data-ttu-id="7f171-103">Crea un piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="7f171-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="7f171-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f171-104">SYNTAX</span></span>

### <span data-ttu-id="7f171-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f171-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f171-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7f171-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f171-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="7f171-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f171-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f171-108">DESCRIPTION</span></span>
<span data-ttu-id="7f171-109">Il cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** crea un piano di ripristino di un sito di Azure, nel Vault di Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="7f171-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="7f171-110">Un piano di ripristino raccoglie le macchine virtuali appartenenti a un'applicazione in un'unità per consentire loro di essere recuperate insieme.</span><span class="sxs-lookup"><span data-stu-id="7f171-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="7f171-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f171-111">EXAMPLES</span></span>

### <span data-ttu-id="7f171-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f171-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="7f171-113">Avvia l'operazione di creazione del piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f171-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7f171-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f171-114">PARAMETERS</span></span>

### <span data-ttu-id="7f171-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="7f171-115">-Azure</span></span>
<span data-ttu-id="7f171-116">Parametro switch specifica lo scenario per il ripristino di emergenza di Azure in Azure, la creazione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f171-117">-DefaultProfile</span></span>
<span data-ttu-id="7f171-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f171-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7f171-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="7f171-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="7f171-120">Specifica il modello di distribuzione di failover (Classic o Resource Manager) degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f171-121">-Name</span></span>
<span data-ttu-id="7f171-122">Nome del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-123">-Path</span><span class="sxs-lookup"><span data-stu-id="7f171-123">-Path</span></span>
<span data-ttu-id="7f171-124">Specifica il percorso del file JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="7f171-125">Per creare il piano di ripristino, è possibile usare un JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7f171-126">-PrimaryFabric</span></span>
<span data-ttu-id="7f171-127">Specifica l'oggetto del tessuto ASR per il tessuto ASR principale degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="7f171-128">-RecoveryFabric</span></span>
<span data-ttu-id="7f171-129">Specifica l'oggetto del tessuto ASR per il tessuto ASR di ripristino degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7f171-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7f171-131">Elenco di elementi protetti per la replica da aggiungere al primo gruppo del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f171-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f171-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f171-132">-Confirm</span></span>
<span data-ttu-id="7f171-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f171-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f171-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f171-134">-WhatIf</span></span>
<span data-ttu-id="7f171-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f171-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f171-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f171-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f171-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f171-137">CommonParameters</span></span>
<span data-ttu-id="7f171-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f171-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f171-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f171-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f171-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f171-140">INPUTS</span></span>

### <span data-ttu-id="7f171-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="7f171-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="7f171-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f171-142">OUTPUTS</span></span>

### <span data-ttu-id="7f171-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7f171-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7f171-144">Note</span><span class="sxs-lookup"><span data-stu-id="7f171-144">NOTES</span></span>

## <span data-ttu-id="7f171-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f171-145">RELATED LINKS</span></span>

[<span data-ttu-id="7f171-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f171-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7f171-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f171-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7f171-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f171-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


