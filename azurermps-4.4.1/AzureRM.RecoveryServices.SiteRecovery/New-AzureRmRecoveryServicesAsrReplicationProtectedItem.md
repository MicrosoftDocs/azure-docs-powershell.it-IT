---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513075"
---
# <span data-ttu-id="30f57-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30f57-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="30f57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30f57-102">SYNOPSIS</span></span>
<span data-ttu-id="30f57-103">Abilita la replica per un elemento protettivo ASR creando un elemento protetto da replica</span><span class="sxs-lookup"><span data-stu-id="30f57-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30f57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30f57-104">SYNTAX</span></span>

### <span data-ttu-id="30f57-105">Disabler (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30f57-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30f57-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="30f57-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30f57-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="30f57-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f57-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="30f57-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30f57-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30f57-109">DESCRIPTION</span></span>
<span data-ttu-id="30f57-110">Il cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="30f57-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="30f57-111">Usa questo cmdlet per abilitare la replica per un elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="30f57-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="30f57-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30f57-112">EXAMPLES</span></span>

### <span data-ttu-id="30f57-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30f57-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="30f57-114">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="30f57-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="30f57-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30f57-115">PARAMETERS</span></span>

### <span data-ttu-id="30f57-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="30f57-116">-Name</span></span>
<span data-ttu-id="30f57-117">Specifica un nome per l'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="30f57-117">Specifies a name for the ASR replication protected item.</span></span>

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

### <span data-ttu-id="30f57-118">-OS</span><span class="sxs-lookup"><span data-stu-id="30f57-118">-OS</span></span>
<span data-ttu-id="30f57-119">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="30f57-119">Specifies the operating system family.</span></span>
<span data-ttu-id="30f57-120">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="30f57-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="30f57-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="30f57-121">-OSDiskName</span></span>
<span data-ttu-id="30f57-122">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30f57-122">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="30f57-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="30f57-123">-ProtectableItem</span></span>
<span data-ttu-id="30f57-124">Specifica l'oggetto elemento protetto ASR per cui viene abilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="30f57-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="30f57-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="30f57-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="30f57-126">Specifica l'oggetto mapping del contenitore di protezione ASR che corrisponde ai criteri di replica da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="30f57-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="30f57-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30f57-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="30f57-128">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="30f57-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="30f57-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="30f57-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="30f57-130">Specifica l'identificatore ARM del gruppo di risorse in cui verrà creata la macchina virtuale in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="30f57-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="30f57-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="30f57-131">-WaitForCompletion</span></span>
<span data-ttu-id="30f57-132">Specifica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="30f57-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="30f57-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30f57-133">-Confirm</span></span>
<span data-ttu-id="30f57-134">Richiede la conferma prima di avviare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="30f57-134">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="30f57-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f57-135">-WhatIf</span></span>
<span data-ttu-id="30f57-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f57-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f57-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f57-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f57-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f57-138">CommonParameters</span></span>
<span data-ttu-id="30f57-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f57-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f57-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f57-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f57-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30f57-141">INPUTS</span></span>

### <span data-ttu-id="30f57-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="30f57-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="30f57-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30f57-143">OUTPUTS</span></span>

### <span data-ttu-id="30f57-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="30f57-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30f57-145">Note</span><span class="sxs-lookup"><span data-stu-id="30f57-145">NOTES</span></span>

## <span data-ttu-id="30f57-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30f57-146">RELATED LINKS</span></span>

[<span data-ttu-id="30f57-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30f57-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="30f57-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30f57-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="30f57-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30f57-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
