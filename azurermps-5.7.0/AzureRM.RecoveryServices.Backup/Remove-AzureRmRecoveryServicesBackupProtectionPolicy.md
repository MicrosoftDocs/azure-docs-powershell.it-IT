---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509720"
---
# <span data-ttu-id="3f5ea-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f5ea-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="3f5ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5ea-103">Elimina i criteri di protezione del backup da un Vault.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f5ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f5ea-104">SYNTAX</span></span>

### <span data-ttu-id="3f5ea-105">PolicyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f5ea-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5ea-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="3f5ea-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f5ea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f5ea-107">DESCRIPTION</span></span>
<span data-ttu-id="3f5ea-108">Il cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** Elimina i criteri di backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="3f5ea-109">Prima di poter eliminare un criterio di protezione del backup, il criterio non deve contenere elementi di backup associati.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="3f5ea-110">Prima di eliminare il criterio, verificare che ogni elemento associato sia associato ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="3f5ea-111">Per associare un altro criterio a un elemento di backup, usare il cmdlet Enable-AzureRmRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="3f5ea-112">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3f5ea-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f5ea-113">EXAMPLES</span></span>

### <span data-ttu-id="3f5ea-114">Esempio 1: rimuovere un criterio</span><span class="sxs-lookup"><span data-stu-id="3f5ea-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="3f5ea-115">Il primo comando consente di ottenere i criteri di protezione del backup denominati NewPolicy e di archiviarli nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="3f5ea-116">Il secondo comando rimuove l'oggetto Policy in $Pol.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="3f5ea-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f5ea-117">PARAMETERS</span></span>

### <span data-ttu-id="3f5ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5ea-118">-DefaultProfile</span></span>
<span data-ttu-id="3f5ea-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f5ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3f5ea-120">-Force</span></span>
<span data-ttu-id="3f5ea-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f5ea-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f5ea-122">-Name</span></span>
<span data-ttu-id="3f5ea-123">Specifica il nome dei criteri di protezione del backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5ea-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f5ea-124">-PassThru</span></span>
<span data-ttu-id="3f5ea-125">Restituire il criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="3f5ea-126">-Policy</span><span class="sxs-lookup"><span data-stu-id="3f5ea-126">-Policy</span></span>
<span data-ttu-id="3f5ea-127">Specifica i criteri di protezione del backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="3f5ea-128">Per ottenere un oggetto **BackupPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5ea-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f5ea-129">-Confirm</span></span>
<span data-ttu-id="3f5ea-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f5ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5ea-131">-WhatIf</span></span>
<span data-ttu-id="3f5ea-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f5ea-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f5ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5ea-134">CommonParameters</span></span>
<span data-ttu-id="3f5ea-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5ea-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f5ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5ea-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f5ea-137">INPUTS</span></span>

### <span data-ttu-id="3f5ea-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="3f5ea-138">PolicyBase</span></span>
<span data-ttu-id="3f5ea-139">Il parametro ' Policy ' accetta il valore di tipo ' PolicyBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3f5ea-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="3f5ea-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f5ea-140">OUTPUTS</span></span>

## <span data-ttu-id="3f5ea-141">Note</span><span class="sxs-lookup"><span data-stu-id="3f5ea-141">NOTES</span></span>

## <span data-ttu-id="3f5ea-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f5ea-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f5ea-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f5ea-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3f5ea-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f5ea-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3f5ea-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f5ea-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


