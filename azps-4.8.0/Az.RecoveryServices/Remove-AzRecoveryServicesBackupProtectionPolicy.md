---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188278"
---
# <span data-ttu-id="b4ebd-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4ebd-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b4ebd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ebd-103">Elimina i criteri di protezione del backup da un Vault.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="b4ebd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4ebd-104">SYNTAX</span></span>

### <span data-ttu-id="b4ebd-105">PolicyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4ebd-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ebd-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="b4ebd-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ebd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="b4ebd-108">Il cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** Elimina i criteri di backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="b4ebd-109">Prima di poter eliminare un criterio di protezione del backup, il criterio non deve contenere elementi di backup associati.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="b4ebd-110">Prima di eliminare il criterio, verificare che ogni elemento associato sia associato ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="b4ebd-111">Per associare un altro criterio a un elemento di backup, usare il cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="b4ebd-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b4ebd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4ebd-113">EXAMPLES</span></span>

### <span data-ttu-id="b4ebd-114">Esempio 1: rimuovere un criterio</span><span class="sxs-lookup"><span data-stu-id="b4ebd-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="b4ebd-115">Il primo comando consente di ottenere i criteri di protezione del backup denominati NewPolicy e di archiviarli nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="b4ebd-116">Il secondo comando rimuove l'oggetto Policy in $Pol.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="b4ebd-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b4ebd-117">Example 2</span></span>

<span data-ttu-id="b4ebd-118">Elimina i criteri di protezione del backup da un Vault.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="b4ebd-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b4ebd-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="b4ebd-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4ebd-120">PARAMETERS</span></span>

### <span data-ttu-id="b4ebd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ebd-121">-DefaultProfile</span></span>
<span data-ttu-id="b4ebd-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ebd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b4ebd-123">-Force</span></span>
<span data-ttu-id="b4ebd-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4ebd-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4ebd-125">-Name</span></span>
<span data-ttu-id="b4ebd-126">Specifica il nome dei criteri di protezione del backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="b4ebd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ebd-127">-PassThru</span></span>
<span data-ttu-id="b4ebd-128">Restituire il criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="b4ebd-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="b4ebd-129">-Policy</span></span>
<span data-ttu-id="b4ebd-130">Specifica i criteri di protezione del backup da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="b4ebd-131">Per ottenere un oggetto **BackupPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="b4ebd-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b4ebd-132">-VaultId</span></span>
<span data-ttu-id="b4ebd-133">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b4ebd-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4ebd-134">-Confirm</span></span>
<span data-ttu-id="b4ebd-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ebd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ebd-136">-WhatIf</span></span>
<span data-ttu-id="b4ebd-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="b4ebd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ebd-138">CommonParameters</span></span>
<span data-ttu-id="b4ebd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ebd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ebd-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4ebd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ebd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4ebd-141">INPUTS</span></span>

### <span data-ttu-id="b4ebd-142">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b4ebd-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="b4ebd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b4ebd-143">System.String</span></span>

## <span data-ttu-id="b4ebd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4ebd-144">OUTPUTS</span></span>

### <span data-ttu-id="b4ebd-145">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b4ebd-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="b4ebd-146">Note</span><span class="sxs-lookup"><span data-stu-id="b4ebd-146">NOTES</span></span>

## <span data-ttu-id="b4ebd-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4ebd-147">RELATED LINKS</span></span>

[<span data-ttu-id="b4ebd-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4ebd-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b4ebd-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4ebd-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b4ebd-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4ebd-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

