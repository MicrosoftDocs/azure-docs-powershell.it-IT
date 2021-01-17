---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475000"
---
# <span data-ttu-id="731ac-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="731ac-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="731ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="731ac-102">SYNOPSIS</span></span>
<span data-ttu-id="731ac-103">Crea un piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="731ac-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="731ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="731ac-104">SYNTAX</span></span>

### <span data-ttu-id="731ac-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="731ac-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731ac-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="731ac-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731ac-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="731ac-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731ac-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="731ac-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="731ac-109">DESCRIPTION</span></span>
<span data-ttu-id="731ac-110">Il cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** crea un piano di ripristino di un sito di Azure, nel Vault di Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="731ac-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="731ac-111">Un piano di ripristino raccoglie le macchine virtuali appartenenti a un'applicazione in un'unità per consentire loro di essere recuperate insieme.</span><span class="sxs-lookup"><span data-stu-id="731ac-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="731ac-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="731ac-112">EXAMPLES</span></span>

### <span data-ttu-id="731ac-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="731ac-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="731ac-114">Avvia l'operazione di creazione del piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="731ac-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="731ac-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="731ac-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="731ac-116">Avvia l'operazione di creazione del piano di ripristino per Azure zone in elementi replicati zona e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="731ac-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="731ac-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="731ac-117">PARAMETERS</span></span>

### <span data-ttu-id="731ac-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="731ac-118">-Azure</span></span>
<span data-ttu-id="731ac-119">Parametro switch specifica lo scenario per il ripristino di emergenza di Azure in Azure, la creazione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="731ac-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="731ac-120">-AzureZoneToZone</span></span>
<span data-ttu-id="731ac-121">Parametro switch specifica la creazione dell'elemento replicato nello scenario di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="731ac-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731ac-122">-DefaultProfile</span></span>
<span data-ttu-id="731ac-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="731ac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="731ac-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="731ac-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="731ac-125">Specifica il modello di distribuzione di failover (Classic o Resource Manager) degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="731ac-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="731ac-126">-Name</span></span>
<span data-ttu-id="731ac-127">Nome del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-128">-Path</span><span class="sxs-lookup"><span data-stu-id="731ac-128">-Path</span></span>
<span data-ttu-id="731ac-129">Specifica il percorso del file JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="731ac-130">Per creare il piano di ripristino, è possibile usare un JSON per la definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="731ac-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="731ac-131">-PrimaryFabric</span></span>
<span data-ttu-id="731ac-132">Specifica l'oggetto del tessuto ASR per il tessuto ASR principale degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="731ac-133">-PrimaryZone</span></span>
<span data-ttu-id="731ac-134">Specifica l'area disponibilità primaria degli elementi protetti per la replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="731ac-135">-RecoveryFabric</span></span>
<span data-ttu-id="731ac-136">Specifica l'oggetto del tessuto ASR per il tessuto ASR di ripristino degli elementi protetti della replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="731ac-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="731ac-137">-RecoveryZone</span></span>
<span data-ttu-id="731ac-138">Specifica l'area disponibilità primaria degli elementi protetti per la replica che faranno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="731ac-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="731ac-140">Elenco di elementi protetti per la replica da aggiungere al primo gruppo del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="731ac-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731ac-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="731ac-141">-Confirm</span></span>
<span data-ttu-id="731ac-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="731ac-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731ac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731ac-143">-WhatIf</span></span>
<span data-ttu-id="731ac-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="731ac-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="731ac-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="731ac-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731ac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731ac-146">CommonParameters</span></span>
<span data-ttu-id="731ac-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731ac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731ac-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="731ac-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731ac-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="731ac-149">INPUTS</span></span>

### <span data-ttu-id="731ac-150">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="731ac-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="731ac-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="731ac-151">OUTPUTS</span></span>

### <span data-ttu-id="731ac-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="731ac-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="731ac-153">Note</span><span class="sxs-lookup"><span data-stu-id="731ac-153">NOTES</span></span>

## <span data-ttu-id="731ac-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="731ac-154">RELATED LINKS</span></span>

[<span data-ttu-id="731ac-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="731ac-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="731ac-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="731ac-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="731ac-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="731ac-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


