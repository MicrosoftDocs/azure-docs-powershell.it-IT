---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520348"
---
# <span data-ttu-id="d1ebd-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d1ebd-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d1ebd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ebd-103">Crea un piano di ripristino del sito nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ebd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1ebd-104">SYNTAX</span></span>

### <span data-ttu-id="d1ebd-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1ebd-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ebd-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d1ebd-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ebd-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="d1ebd-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ebd-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="d1ebd-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ebd-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="d1ebd-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ebd-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="d1ebd-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1ebd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1ebd-111">DESCRIPTION</span></span>
<span data-ttu-id="d1ebd-112">Il cmdlet **New-AzureRmSiteRecoveryRecoveryPlan** crea un piano di ripristino in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="d1ebd-113">Un piano di ripristino raccoglie le macchine virtuali in un gruppo per scopi di failover e ripristino.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="d1ebd-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1ebd-114">EXAMPLES</span></span>

### <span data-ttu-id="d1ebd-115">Esempio 1: aggiungere un piano di ripristino a un Vault di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="d1ebd-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="d1ebd-116">Questo comando aggiunge il piano di ripristino denominato RecoveryPlan.xml all'archivio di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d1ebd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1ebd-117">PARAMETERS</span></span>

### <span data-ttu-id="d1ebd-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="d1ebd-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ebd-119">-DefaultProfile</span></span>
<span data-ttu-id="d1ebd-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ebd-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="d1ebd-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1ebd-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-123">-Path</span><span class="sxs-lookup"><span data-stu-id="d1ebd-123">-Path</span></span>
<span data-ttu-id="d1ebd-124">Specifica il percorso del file del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-124">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="d1ebd-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="d1ebd-125">-PrimaryFabric</span></span>
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

### <span data-ttu-id="d1ebd-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="d1ebd-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="d1ebd-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="d1ebd-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d1ebd-129">-RecoveryFabric</span></span>
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

### <span data-ttu-id="d1ebd-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d1ebd-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ebd-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d1ebd-131">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="d1ebd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ebd-132">CommonParameters</span></span>
<span data-ttu-id="d1ebd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ebd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ebd-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ebd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ebd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1ebd-135">INPUTS</span></span>

### <span data-ttu-id="d1ebd-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="d1ebd-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="d1ebd-137">Il parametro ' ProtectionEntityList ' accetta il valore di tipo ' ASRProtectionEntity []' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d1ebd-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="d1ebd-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="d1ebd-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="d1ebd-139">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem []' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d1ebd-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="d1ebd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1ebd-140">OUTPUTS</span></span>

## <span data-ttu-id="d1ebd-141">Note</span><span class="sxs-lookup"><span data-stu-id="d1ebd-141">NOTES</span></span>

## <span data-ttu-id="d1ebd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1ebd-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1ebd-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d1ebd-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d1ebd-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d1ebd-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d1ebd-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d1ebd-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


