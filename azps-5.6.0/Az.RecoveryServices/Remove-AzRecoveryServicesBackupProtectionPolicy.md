---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 4723fd3087b2f547659e72c1af6b0f5cb7764cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953118"
---
# <span data-ttu-id="4a3a0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3a0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="4a3a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a0-103">Elimina i criteri di protezione del backup da un vault.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="4a3a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a3a0-104">SYNTAX</span></span>

### <span data-ttu-id="4a3a0-105">PolicyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a3a0-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3a0-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="4a3a0-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3a0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a3a0-107">DESCRIPTION</span></span>
<span data-ttu-id="4a3a0-108">Il cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** elimina i criteri di backup per un vault.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="4a3a0-109">Per poter eliminare un criterio di protezione del backup, è necessario che al criterio non sia associato alcun elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="4a3a0-110">Prima di eliminare i criteri, assicurarsi che ogni elemento associato sia associato ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="4a3a0-111">Per associare un altro criterio a un elemento di backup, usare il cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="4a3a0-112">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4a3a0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a3a0-113">EXAMPLES</span></span>

### <span data-ttu-id="4a3a0-114">Esempio 1: Rimuovere un criterio</span><span class="sxs-lookup"><span data-stu-id="4a3a0-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="4a3a0-115">Il primo comando ottiene il criterio di protezione backup denominato NewPolicy e quindi lo archivia nella $Pol variabile.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="4a3a0-116">Il secondo comando rimuove l'oggetto criterio in $Pol.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="4a3a0-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4a3a0-117">Example 2</span></span>

<span data-ttu-id="4a3a0-118">Elimina i criteri di protezione del backup da un vault.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="4a3a0-119">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="4a3a0-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="4a3a0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a3a0-120">PARAMETERS</span></span>

### <span data-ttu-id="4a3a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3a0-121">-DefaultProfile</span></span>
<span data-ttu-id="4a3a0-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3a0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4a3a0-123">-Force</span></span>
<span data-ttu-id="4a3a0-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a3a0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4a3a0-125">-Name</span></span>
<span data-ttu-id="4a3a0-126">Specifica il nome del criterio di protezione backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a3a0-127">-PassThru</span></span>
<span data-ttu-id="4a3a0-128">Restituire i criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="4a3a0-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="4a3a0-129">-Policy</span></span>
<span data-ttu-id="4a3a0-130">Specifica i criteri di protezione del backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="4a3a0-131">Per ottenere un **oggetto BackupPolicy,** usare il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a0-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4a3a0-132">-VaultId</span></span>
<span data-ttu-id="4a3a0-133">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-133">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a3a0-134">-Confirm</span></span>
<span data-ttu-id="4a3a0-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3a0-136">-WhatIf</span></span>
<span data-ttu-id="4a3a0-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="4a3a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a0-138">CommonParameters</span></span>
<span data-ttu-id="4a3a0-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a0-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a3a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a0-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a3a0-141">INPUTS</span></span>

### <span data-ttu-id="4a3a0-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4a3a0-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="4a3a0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4a3a0-143">System.String</span></span>

## <span data-ttu-id="4a3a0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a3a0-144">OUTPUTS</span></span>

### <span data-ttu-id="4a3a0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4a3a0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="4a3a0-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a3a0-146">NOTES</span></span>

## <span data-ttu-id="4a3a0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a3a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="4a3a0-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3a0-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4a3a0-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3a0-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4a3a0-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3a0-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


