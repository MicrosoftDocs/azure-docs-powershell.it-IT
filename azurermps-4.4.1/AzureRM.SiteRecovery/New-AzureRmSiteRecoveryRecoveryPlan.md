---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686779"
---
# <span data-ttu-id="d3c95-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3c95-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d3c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3c95-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c95-103">Crea un piano di ripristino del sito nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="d3c95-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3c95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3c95-104">SYNTAX</span></span>

### <span data-ttu-id="d3c95-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3c95-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3c95-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d3c95-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c95-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="d3c95-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c95-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="d3c95-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c95-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="d3c95-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c95-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="d3c95-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3c95-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3c95-111">DESCRIPTION</span></span>
<span data-ttu-id="d3c95-112">Il cmdlet **New-AzureRmSiteRecoveryRecoveryPlan** crea un piano di ripristino in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d3c95-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="d3c95-113">Un piano di ripristino raccoglie le macchine virtuali in un gruppo per scopi di failover e ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3c95-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="d3c95-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3c95-114">EXAMPLES</span></span>

### <span data-ttu-id="d3c95-115">Esempio 1: aggiungere un piano di ripristino a un Vault di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="d3c95-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="d3c95-116">Questo comando aggiunge il piano di ripristino denominato RecoveryPlan.xml all'archivio di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c95-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d3c95-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3c95-117">PARAMETERS</span></span>

### <span data-ttu-id="d3c95-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="d3c95-118">-Azure</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="d3c95-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3c95-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-121">-Path</span><span class="sxs-lookup"><span data-stu-id="d3c95-121">-Path</span></span>
<span data-ttu-id="d3c95-122">Specifica il percorso del file del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3c95-122">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="d3c95-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="d3c95-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="d3c95-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-125">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="d3c95-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="d3c95-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d3c95-127">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d3c95-128">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-129">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3c95-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c95-130">-DefaultProfile</span></span>
<span data-ttu-id="d3c95-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c95-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c95-132">CommonParameters</span></span>
<span data-ttu-id="d3c95-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c95-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c95-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c95-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3c95-135">INPUTS</span></span>

### <span data-ttu-id="d3c95-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="d3c95-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="d3c95-137">Il parametro ' ProtectionEntityList ' accetta il valore di tipo ' ASRProtectionEntity []' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c95-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="d3c95-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="d3c95-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="d3c95-139">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem []' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c95-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="d3c95-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3c95-140">OUTPUTS</span></span>

## <span data-ttu-id="d3c95-141">Note</span><span class="sxs-lookup"><span data-stu-id="d3c95-141">NOTES</span></span>

## <span data-ttu-id="d3c95-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3c95-142">RELATED LINKS</span></span>

[<span data-ttu-id="d3c95-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3c95-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d3c95-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3c95-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d3c95-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d3c95-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


