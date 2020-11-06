---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509768"
---
# <span data-ttu-id="9b432-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9b432-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9b432-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b432-102">SYNOPSIS</span></span>
<span data-ttu-id="9b432-103">Consente di eseguire il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="9b432-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b432-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b432-104">SYNTAX</span></span>

### <span data-ttu-id="9b432-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b432-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b432-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="9b432-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b432-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="9b432-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b432-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b432-108">DESCRIPTION</span></span>
<span data-ttu-id="9b432-109">Il cmdlet **Enable-AzureRmRecoveryServicesBackupProtection** imposta i criteri di protezione di Azure Backup su un elemento.</span><span class="sxs-lookup"><span data-stu-id="9b432-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="9b432-110">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9b432-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9b432-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b432-111">EXAMPLES</span></span>

### <span data-ttu-id="9b432-112">Esempio 1: abilitare la protezione del backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="9b432-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="9b432-113">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="9b432-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="9b432-114">Il secondo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM denominata V2VM usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="9b432-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="9b432-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b432-115">PARAMETERS</span></span>

### <span data-ttu-id="9b432-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b432-116">-DefaultProfile</span></span>
<span data-ttu-id="9b432-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b432-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b432-118">-Elemento</span><span class="sxs-lookup"><span data-stu-id="9b432-118">-Item</span></span>
<span data-ttu-id="9b432-119">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="9b432-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="9b432-120">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="9b432-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b432-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b432-121">-Name</span></span>
<span data-ttu-id="9b432-122">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="9b432-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b432-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="9b432-123">-Policy</span></span>
<span data-ttu-id="9b432-124">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="9b432-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="9b432-125">Per ottenere un oggetto **AzureRmRecoveryServicesBackupProtectionPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9b432-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b432-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b432-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b432-127">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b432-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9b432-128">Specificare questo parametro solo per le macchine virtuali ARM.</span><span class="sxs-lookup"><span data-stu-id="9b432-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b432-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9b432-129">-ServiceName</span></span>
<span data-ttu-id="9b432-130">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="9b432-130">Specifies the service name.</span></span>
<span data-ttu-id="9b432-131">Specifica questo parametro solo per le macchine virtuali ASM.</span><span class="sxs-lookup"><span data-stu-id="9b432-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b432-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b432-132">-Confirm</span></span>
<span data-ttu-id="9b432-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b432-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b432-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b432-134">-WhatIf</span></span>
<span data-ttu-id="9b432-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b432-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b432-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b432-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b432-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b432-137">CommonParameters</span></span>
<span data-ttu-id="9b432-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b432-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b432-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b432-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b432-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b432-140">INPUTS</span></span>

### <span data-ttu-id="9b432-141">ItemBase</span><span class="sxs-lookup"><span data-stu-id="9b432-141">ItemBase</span></span>
<span data-ttu-id="9b432-142">Il parametro ' Item ' accetta il valore di tipo ' ItemBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9b432-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="9b432-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b432-143">OUTPUTS</span></span>

### <span data-ttu-id="9b432-144">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9b432-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9b432-145">Note</span><span class="sxs-lookup"><span data-stu-id="9b432-145">NOTES</span></span>

## <span data-ttu-id="9b432-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b432-146">RELATED LINKS</span></span>

[<span data-ttu-id="9b432-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9b432-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9b432-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b432-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


