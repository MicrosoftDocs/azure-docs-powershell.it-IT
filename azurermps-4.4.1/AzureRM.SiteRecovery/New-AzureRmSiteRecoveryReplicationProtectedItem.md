---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510308"
---
# <span data-ttu-id="67879-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67879-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="67879-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67879-102">SYNOPSIS</span></span>
<span data-ttu-id="67879-103">Abilita la replica per un elemento protettivo creando un elemento protetto</span><span class="sxs-lookup"><span data-stu-id="67879-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67879-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67879-104">SYNTAX</span></span>

### <span data-ttu-id="67879-105">Disabler (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67879-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67879-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="67879-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67879-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="67879-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67879-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="67879-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67879-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67879-109">DESCRIPTION</span></span>
<span data-ttu-id="67879-110">Il cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="67879-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="67879-111">Usa questo cmdlet per abilitare la replica per un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="67879-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="67879-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67879-112">EXAMPLES</span></span>

## <span data-ttu-id="67879-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67879-113">PARAMETERS</span></span>

### <span data-ttu-id="67879-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="67879-114">-Name</span></span>
<span data-ttu-id="67879-115">Specifica il nome dell'elemento protetto della replica di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="67879-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-116">-OS</span><span class="sxs-lookup"><span data-stu-id="67879-116">-OS</span></span>
<span data-ttu-id="67879-117">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="67879-117">Specifies the operating system family.</span></span>
<span data-ttu-id="67879-118">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="67879-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="67879-119">-OSDiskName</span></span>
<span data-ttu-id="67879-120">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67879-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="67879-121">-ProtectableItem</span></span>
<span data-ttu-id="67879-122">Specifica l'elemento protetto per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="67879-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67879-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="67879-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="67879-124">Specifica l'oggetto di mapping del contenitore di protezione del sito di Azure da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="67879-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="67879-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="67879-126">Specifica l'ID dell'account di archiviazione di Azure a cui viene replicato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67879-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="67879-127">-WaitForCompletion</span></span>
<span data-ttu-id="67879-128">Indica che il cmdlet attende il completamento.</span><span class="sxs-lookup"><span data-stu-id="67879-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67879-129">-Confirm</span></span>
<span data-ttu-id="67879-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67879-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67879-131">-WhatIf</span></span>
<span data-ttu-id="67879-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67879-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="67879-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67879-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67879-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67879-134">-DefaultProfile</span></span>
<span data-ttu-id="67879-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67879-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67879-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67879-136">CommonParameters</span></span>
<span data-ttu-id="67879-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67879-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67879-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67879-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67879-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67879-139">INPUTS</span></span>

### <span data-ttu-id="67879-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="67879-140">ASRProtectableItem</span></span>
<span data-ttu-id="67879-141">Il parametro ' ProtectableItem ' accetta il valore di tipo ' ASRProtectableItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="67879-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="67879-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67879-142">OUTPUTS</span></span>

### <span data-ttu-id="67879-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="67879-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67879-144">Note</span><span class="sxs-lookup"><span data-stu-id="67879-144">NOTES</span></span>

## <span data-ttu-id="67879-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67879-145">RELATED LINKS</span></span>

[<span data-ttu-id="67879-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67879-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="67879-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67879-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="67879-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67879-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
