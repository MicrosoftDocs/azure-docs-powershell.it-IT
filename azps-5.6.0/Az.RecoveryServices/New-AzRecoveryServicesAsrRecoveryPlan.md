---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985695"
---
# <span data-ttu-id="7d3c1-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7d3c1-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7d3c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3c1-103">Crea un piano di ripristino a matrice.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="7d3c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d3c1-104">SYNTAX</span></span>

### <span data-ttu-id="7d3c1-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d3c1-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3c1-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7d3c1-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3c1-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="7d3c1-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3c1-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="7d3c1-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3c1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d3c1-109">DESCRIPTION</span></span>
<span data-ttu-id="7d3c1-110">Il cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** crea un piano di ripristino del sito di Azure nella vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="7d3c1-111">Un piano di ripristino raccoglie le macchine virtuali appartenenti a un'applicazione in un'unità per consentirle di recuperarle insieme.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="7d3c1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d3c1-112">EXAMPLES</span></span>

### <span data-ttu-id="7d3c1-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d3c1-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="7d3c1-114">Avvia l'operazione di creazione del piano di ripristino con i parametri specificati e restituisce il processo asr usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7d3c1-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d3c1-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="7d3c1-116">Avvia l'operazione di creazione del piano di ripristino per l'area di Azure per l'area degli elementi replicati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7d3c1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d3c1-117">PARAMETERS</span></span>

### <span data-ttu-id="7d3c1-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="7d3c1-118">-Azure</span></span>
<span data-ttu-id="7d3c1-119">Il parametro switch specifica lo scenario per azure per il ripristino di emergenza e la creazione di piani di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="7d3c1-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="7d3c1-120">-AzureZoneToZone</span></span>
<span data-ttu-id="7d3c1-121">Parametro Switch specifica la creazione dell'elemento replicato nell'area azure in uno scenario di zona.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="7d3c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3c1-122">-DefaultProfile</span></span>
<span data-ttu-id="7d3c1-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7d3c1-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="7d3c1-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="7d3c1-125">Specifica il modello di distribuzione di failover (classico o manager delle risorse) degli elementi protetti da replica che fanno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7d3c1-126">-Name</span></span>
<span data-ttu-id="7d3c1-127">Nome del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-128">-Path</span><span class="sxs-lookup"><span data-stu-id="7d3c1-128">-Path</span></span>
<span data-ttu-id="7d3c1-129">Specifica il percorso del file JSON della definizione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="7d3c1-130">La definizione json di un piano di ripristino può essere usata per creare il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7d3c1-131">-PrimaryFabric</span></span>
<span data-ttu-id="7d3c1-132">Specifica l'oggetto tessuto ASR per il tessuto ASR primario degli elementi protetti da replica che fanno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="7d3c1-133">-PrimaryZone</span></span>
<span data-ttu-id="7d3c1-134">Specifica l'area di accesso primario degli elementi protetti da replica che fanno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="7d3c1-135">-RecoveryFabric</span></span>
<span data-ttu-id="7d3c1-136">Specifica l'oggetto tessuto ASR per il tessuto di recupero ASR degli elementi protetti da replica che fanno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="7d3c1-137">-RecoveryZone</span></span>
<span data-ttu-id="7d3c1-138">Specifica l'area di accesso primario degli elementi protetti da replica che fanno parte di questo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d3c1-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7d3c1-140">Elenco di elementi protetti da replica da aggiungere al primo gruppo del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="7d3c1-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d3c1-141">-Confirm</span></span>
<span data-ttu-id="7d3c1-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3c1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3c1-143">-WhatIf</span></span>
<span data-ttu-id="7d3c1-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d3c1-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d3c1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3c1-146">CommonParameters</span></span>
<span data-ttu-id="7d3c1-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3c1-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d3c1-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3c1-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d3c1-149">INPUTS</span></span>

### <span data-ttu-id="7d3c1-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="7d3c1-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="7d3c1-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d3c1-151">OUTPUTS</span></span>

### <span data-ttu-id="7d3c1-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7d3c1-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7d3c1-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d3c1-153">NOTES</span></span>

## <span data-ttu-id="7d3c1-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d3c1-154">RELATED LINKS</span></span>

[<span data-ttu-id="7d3c1-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7d3c1-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7d3c1-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7d3c1-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7d3c1-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7d3c1-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


