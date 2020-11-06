---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520346"
---
# <span data-ttu-id="58de2-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="58de2-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="58de2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58de2-102">SYNOPSIS</span></span>
<span data-ttu-id="58de2-103">Abilita la replica per un elemento protettivo creando un elemento protetto</span><span class="sxs-lookup"><span data-stu-id="58de2-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58de2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58de2-104">SYNTAX</span></span>

### <span data-ttu-id="58de2-105">Disabler (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58de2-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58de2-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="58de2-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58de2-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="58de2-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58de2-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="58de2-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58de2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58de2-109">DESCRIPTION</span></span>
<span data-ttu-id="58de2-110">Il cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="58de2-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="58de2-111">Usa questo cmdlet per abilitare la replica per un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="58de2-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="58de2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58de2-112">EXAMPLES</span></span>

## <span data-ttu-id="58de2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58de2-113">PARAMETERS</span></span>

### <span data-ttu-id="58de2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58de2-114">-DefaultProfile</span></span>
<span data-ttu-id="58de2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58de2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58de2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="58de2-116">-Name</span></span>
<span data-ttu-id="58de2-117">Specifica il nome dell'elemento protetto della replica di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="58de2-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-118">-OS</span><span class="sxs-lookup"><span data-stu-id="58de2-118">-OS</span></span>
<span data-ttu-id="58de2-119">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="58de2-119">Specifies the operating system family.</span></span>
<span data-ttu-id="58de2-120">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="58de2-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="58de2-121">-OSDiskName</span></span>
<span data-ttu-id="58de2-122">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="58de2-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="58de2-123">-ProtectableItem</span></span>
<span data-ttu-id="58de2-124">Specifica l'elemento protetto per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="58de2-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="58de2-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="58de2-126">Specifica l'oggetto di mapping del contenitore di protezione del sito di Azure da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="58de2-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="58de2-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="58de2-128">Specifica l'ID dell'account di archiviazione di Azure a cui viene replicato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58de2-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="58de2-129">-WaitForCompletion</span></span>
<span data-ttu-id="58de2-130">Indica che il cmdlet attende il completamento.</span><span class="sxs-lookup"><span data-stu-id="58de2-130">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58de2-131">-Confirm</span></span>
<span data-ttu-id="58de2-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58de2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58de2-133">-WhatIf</span></span>
<span data-ttu-id="58de2-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58de2-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="58de2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58de2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58de2-136">CommonParameters</span></span>
<span data-ttu-id="58de2-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58de2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58de2-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58de2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58de2-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58de2-139">INPUTS</span></span>

### <span data-ttu-id="58de2-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="58de2-140">ASRProtectableItem</span></span>
<span data-ttu-id="58de2-141">Il parametro ' ProtectableItem ' accetta il valore di tipo ' ASRProtectableItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="58de2-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="58de2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58de2-142">OUTPUTS</span></span>

### <span data-ttu-id="58de2-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58de2-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58de2-144">Note</span><span class="sxs-lookup"><span data-stu-id="58de2-144">NOTES</span></span>

## <span data-ttu-id="58de2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58de2-145">RELATED LINKS</span></span>

[<span data-ttu-id="58de2-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="58de2-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="58de2-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="58de2-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="58de2-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="58de2-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
