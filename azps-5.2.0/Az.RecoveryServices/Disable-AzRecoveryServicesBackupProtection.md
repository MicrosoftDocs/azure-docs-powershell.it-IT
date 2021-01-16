---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341563"
---
# <span data-ttu-id="e7491-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e7491-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="e7491-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7491-102">SYNOPSIS</span></span>
<span data-ttu-id="e7491-103">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="e7491-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="e7491-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7491-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7491-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7491-105">DESCRIPTION</span></span>
<span data-ttu-id="e7491-106">Il cmdlet **Disable-AzRecoveryServicesBackupProtection Disabilita** la protezione per un elemento protetto da backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7491-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="e7491-107">Questo cmdlet interrompe il backup pianificato regolare di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e7491-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="e7491-108">Questo cmdlet può anche eliminare i punti di ripristino esistenti per l'elemento di backup se eseguito con il parametro RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="e7491-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="e7491-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="e7491-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e7491-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7491-110">EXAMPLES</span></span>

### <span data-ttu-id="e7491-111">Esempio 1: disabilitare la protezione del backup</span><span class="sxs-lookup"><span data-stu-id="e7491-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="e7491-112">Il primo comando ottiene una matrice di contenitori di backup e lo archivia nella matrice $Cont.</span><span class="sxs-lookup"><span data-stu-id="e7491-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="e7491-113">Il secondo comando ottiene l'elemento di backup corrispondente al primo elemento contenitore e lo archivia nella variabile $PI.</span><span class="sxs-lookup"><span data-stu-id="e7491-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="e7491-114">L'ultimo comando Disabilita la protezione del backup per l'elemento in $PI \[ 0 \] , ma mantiene i dati.</span><span class="sxs-lookup"><span data-stu-id="e7491-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="e7491-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e7491-115">Example 2</span></span>

<span data-ttu-id="e7491-116">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="e7491-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="e7491-117">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e7491-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="e7491-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7491-118">PARAMETERS</span></span>

### <span data-ttu-id="e7491-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7491-119">-DefaultProfile</span></span>
<span data-ttu-id="e7491-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7491-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7491-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e7491-121">-Force</span></span>
<span data-ttu-id="e7491-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e7491-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7491-123">-Elemento</span><span class="sxs-lookup"><span data-stu-id="e7491-123">-Item</span></span>
<span data-ttu-id="e7491-124">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="e7491-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="e7491-125">Per ottenere un **AzureRmRecoveryServicesBackupItem**, usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="e7491-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="e7491-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="e7491-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="e7491-127">Indica che questo cmdlet elimina i punti di ripristino esistenti.</span><span class="sxs-lookup"><span data-stu-id="e7491-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

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

### <span data-ttu-id="e7491-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e7491-128">-VaultId</span></span>
<span data-ttu-id="e7491-129">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7491-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e7491-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e7491-130">-Confirm</span></span>
<span data-ttu-id="e7491-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7491-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7491-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7491-132">-WhatIf</span></span>
<span data-ttu-id="e7491-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7491-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7491-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7491-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7491-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7491-135">CommonParameters</span></span>
<span data-ttu-id="e7491-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7491-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7491-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7491-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7491-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7491-138">INPUTS</span></span>

### <span data-ttu-id="e7491-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e7491-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e7491-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e7491-140">System.String</span></span>

## <span data-ttu-id="e7491-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7491-141">OUTPUTS</span></span>

### <span data-ttu-id="e7491-142">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e7491-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e7491-143">Note</span><span class="sxs-lookup"><span data-stu-id="e7491-143">NOTES</span></span>

## <span data-ttu-id="e7491-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7491-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7491-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e7491-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e7491-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e7491-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="e7491-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e7491-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


