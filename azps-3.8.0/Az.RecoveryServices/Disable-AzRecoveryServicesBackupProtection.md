---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865248"
---
# <span data-ttu-id="a8be1-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a8be1-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="a8be1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8be1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8be1-103">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="a8be1-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="a8be1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8be1-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8be1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8be1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8be1-106">Il cmdlet **Disable-AzRecoveryServicesBackupProtection Disabilita** la protezione per un elemento protetto da backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8be1-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="a8be1-107">Questo cmdlet interrompe il backup pianificato regolare di un elemento.</span><span class="sxs-lookup"><span data-stu-id="a8be1-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="a8be1-108">Questo cmdlet può anche eliminare i punti di ripristino esistenti per l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="a8be1-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="a8be1-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="a8be1-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a8be1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8be1-110">EXAMPLES</span></span>

### <span data-ttu-id="a8be1-111">Esempio 1: disabilitare la protezione del backup</span><span class="sxs-lookup"><span data-stu-id="a8be1-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="a8be1-112">Il primo comando ottiene una matrice di contenitori di backup e lo archivia nella matrice $Cont.</span><span class="sxs-lookup"><span data-stu-id="a8be1-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="a8be1-113">Il secondo comando ottiene l'elemento di backup corrispondente al primo elemento contenitore e lo archivia nella variabile $PI.</span><span class="sxs-lookup"><span data-stu-id="a8be1-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="a8be1-114">L'ultimo comando Disabilita la protezione del backup per l'elemento in $PI \[ 0 \] , ma mantiene i dati.</span><span class="sxs-lookup"><span data-stu-id="a8be1-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="a8be1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8be1-115">PARAMETERS</span></span>

### <span data-ttu-id="a8be1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8be1-116">-DefaultProfile</span></span>
<span data-ttu-id="a8be1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8be1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8be1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a8be1-118">-Force</span></span>
<span data-ttu-id="a8be1-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8be1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8be1-120">-Elemento</span><span class="sxs-lookup"><span data-stu-id="a8be1-120">-Item</span></span>
<span data-ttu-id="a8be1-121">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="a8be1-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="a8be1-122">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a8be1-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="a8be1-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="a8be1-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="a8be1-124">Indica che questo cmdlet elimina i punti di ripristino esistenti.</span><span class="sxs-lookup"><span data-stu-id="a8be1-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="a8be1-125">Per eliminare i punti di ripristino archiviati in un secondo momento, eseguire di nuovo questo cmdlet e specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a8be1-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="a8be1-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a8be1-126">-VaultId</span></span>
<span data-ttu-id="a8be1-127">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a8be1-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a8be1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8be1-128">-Confirm</span></span>
<span data-ttu-id="a8be1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8be1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8be1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8be1-130">-WhatIf</span></span>
<span data-ttu-id="a8be1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8be1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8be1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8be1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8be1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8be1-133">CommonParameters</span></span>
<span data-ttu-id="a8be1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8be1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8be1-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8be1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8be1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8be1-136">INPUTS</span></span>

### <span data-ttu-id="a8be1-137">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="a8be1-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="a8be1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8be1-138">System.String</span></span>

## <span data-ttu-id="a8be1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8be1-139">OUTPUTS</span></span>

### <span data-ttu-id="a8be1-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a8be1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a8be1-141">Note</span><span class="sxs-lookup"><span data-stu-id="a8be1-141">NOTES</span></span>

## <span data-ttu-id="a8be1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8be1-142">RELATED LINKS</span></span>

[<span data-ttu-id="a8be1-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a8be1-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="a8be1-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a8be1-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a8be1-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a8be1-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


