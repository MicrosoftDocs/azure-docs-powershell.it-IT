---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513099"
---
# <span data-ttu-id="03f40-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="03f40-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="03f40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03f40-102">SYNOPSIS</span></span>
<span data-ttu-id="03f40-103">Consente di eseguire il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="03f40-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03f40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03f40-104">SYNTAX</span></span>

### <span data-ttu-id="03f40-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03f40-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03f40-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="03f40-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03f40-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="03f40-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03f40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03f40-108">DESCRIPTION</span></span>
<span data-ttu-id="03f40-109">Il cmdlet **Enable-AzureRmRecoveryServicesBackupProtection** imposta i criteri di protezione di Azure Backup su un elemento.</span><span class="sxs-lookup"><span data-stu-id="03f40-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="03f40-110">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="03f40-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="03f40-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03f40-111">EXAMPLES</span></span>

### <span data-ttu-id="03f40-112">Esempio 1: abilitare la protezione del backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="03f40-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="03f40-113">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="03f40-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="03f40-114">Il secondo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM denominata V2VM usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="03f40-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="03f40-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03f40-115">PARAMETERS</span></span>

### <span data-ttu-id="03f40-116">-Elemento</span><span class="sxs-lookup"><span data-stu-id="03f40-116">-Item</span></span>
<span data-ttu-id="03f40-117">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="03f40-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="03f40-118">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="03f40-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03f40-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="03f40-119">-Name</span></span>
<span data-ttu-id="03f40-120">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="03f40-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f40-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="03f40-121">-Policy</span></span>
<span data-ttu-id="03f40-122">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="03f40-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="03f40-123">Per ottenere un oggetto **AzureRmRecoveryServicesBackupProtectionPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="03f40-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03f40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f40-124">-ResourceGroupName</span></span>
<span data-ttu-id="03f40-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03f40-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="03f40-126">Specificare questo parametro solo per le macchine virtuali ARM.</span><span class="sxs-lookup"><span data-stu-id="03f40-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f40-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="03f40-127">-ServiceName</span></span>
<span data-ttu-id="03f40-128">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="03f40-128">Specifies the service name.</span></span>
<span data-ttu-id="03f40-129">Specifica questo parametro solo per le macchine virtuali ASM.</span><span class="sxs-lookup"><span data-stu-id="03f40-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f40-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f40-130">-DefaultProfile</span></span>
<span data-ttu-id="03f40-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03f40-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03f40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f40-132">CommonParameters</span></span>
<span data-ttu-id="03f40-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f40-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f40-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03f40-135">INPUTS</span></span>

### <span data-ttu-id="03f40-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="03f40-136">ItemBase</span></span>
<span data-ttu-id="03f40-137">Il parametro ' Item ' accetta il valore di tipo ' ItemBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="03f40-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="03f40-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03f40-138">OUTPUTS</span></span>

### <span data-ttu-id="03f40-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="03f40-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="03f40-140">Note</span><span class="sxs-lookup"><span data-stu-id="03f40-140">NOTES</span></span>

## <span data-ttu-id="03f40-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03f40-141">RELATED LINKS</span></span>

[<span data-ttu-id="03f40-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="03f40-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="03f40-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="03f40-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


