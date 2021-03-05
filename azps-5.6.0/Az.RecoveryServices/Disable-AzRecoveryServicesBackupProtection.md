---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: bb0f3b18697b3f9e17b8e1744361346e68c47357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960253"
---
# <span data-ttu-id="3d055-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3d055-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="3d055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d055-102">SYNOPSIS</span></span>
<span data-ttu-id="3d055-103">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="3d055-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="3d055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d055-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d055-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d055-105">DESCRIPTION</span></span>
<span data-ttu-id="3d055-106">Il cmdlet **Disable-AzRecoveryServicesBackupProtection** disabilita la protezione per un elemento protetto da backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d055-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="3d055-107">Questo cmdlet interrompe il backup pianificato normale di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3d055-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="3d055-108">Questo cmdlet può anche eliminare i punti di ripristino esistenti per l'elemento di backup se eseguito con il parametro RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="3d055-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="3d055-109">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="3d055-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3d055-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d055-110">EXAMPLES</span></span>

### <span data-ttu-id="3d055-111">Esempio 1: Disabilitare la protezione per il backup</span><span class="sxs-lookup"><span data-stu-id="3d055-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="3d055-112">Il primo comando ottiene una matrice di contenitori di backup e quindi la archivia nella $Cont matrice.</span><span class="sxs-lookup"><span data-stu-id="3d055-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="3d055-113">Il secondo comando recupera l'elemento di backup corrispondente al primo elemento del contenitore e quindi lo archivia nella $PI variabile.</span><span class="sxs-lookup"><span data-stu-id="3d055-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="3d055-114">L'ultimo comando disabilita la protezione del backup per l'elemento di $PI \[ \] 0, ma conserva i dati.</span><span class="sxs-lookup"><span data-stu-id="3d055-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="3d055-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3d055-115">Example 2</span></span>

<span data-ttu-id="3d055-116">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="3d055-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="3d055-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="3d055-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="3d055-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d055-118">PARAMETERS</span></span>

### <span data-ttu-id="3d055-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d055-119">-DefaultProfile</span></span>
<span data-ttu-id="3d055-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d055-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d055-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3d055-121">-Force</span></span>
<span data-ttu-id="3d055-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3d055-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d055-123">-Item</span><span class="sxs-lookup"><span data-stu-id="3d055-123">-Item</span></span>
<span data-ttu-id="3d055-124">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="3d055-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="3d055-125">Per ottenere un **elemento AzureRmRecoveryServicesBackupItem,** usare il cmdlet Get-AzRecoveryServicesBackupItem AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="3d055-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d055-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="3d055-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="3d055-127">Indica che questo cmdlet elimina i punti di ripristino esistenti.</span><span class="sxs-lookup"><span data-stu-id="3d055-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d055-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3d055-128">-VaultId</span></span>
<span data-ttu-id="3d055-129">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d055-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3d055-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d055-130">-Confirm</span></span>
<span data-ttu-id="3d055-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d055-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d055-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d055-132">-WhatIf</span></span>
<span data-ttu-id="3d055-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d055-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d055-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d055-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d055-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d055-135">CommonParameters</span></span>
<span data-ttu-id="3d055-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d055-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d055-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d055-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d055-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d055-138">INPUTS</span></span>

### <span data-ttu-id="3d055-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="3d055-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="3d055-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3d055-140">System.String</span></span>

## <span data-ttu-id="3d055-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d055-141">OUTPUTS</span></span>

### <span data-ttu-id="3d055-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="3d055-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3d055-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d055-143">NOTES</span></span>

## <span data-ttu-id="3d055-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d055-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d055-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3d055-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3d055-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3d055-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="3d055-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d055-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


