---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856577"
---
# <span data-ttu-id="342bb-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="342bb-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="342bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="342bb-102">SYNOPSIS</span></span>
<span data-ttu-id="342bb-103">Reidrata un elemento eliminato temporaneamente</span><span class="sxs-lookup"><span data-stu-id="342bb-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="342bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="342bb-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="342bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="342bb-105">DESCRIPTION</span></span>
<span data-ttu-id="342bb-106">Il cmdlet Undo-AzRecoveryServicesBackupItemDeletion reidrata un elemento eliminato temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="342bb-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="342bb-107">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="342bb-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="342bb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="342bb-108">EXAMPLES</span></span>

### <span data-ttu-id="342bb-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="342bb-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="342bb-110">Il primo comando ottiene una matrice di contenitori di backup e lo archivia nella matrice $Cont.</span><span class="sxs-lookup"><span data-stu-id="342bb-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="342bb-111">Il secondo comando ottiene l'elemento di backup corrispondente al primo elemento contenitore e lo archivia nella variabile $PI.</span><span class="sxs-lookup"><span data-stu-id="342bb-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="342bb-112">Il terzo comando Disabilita la protezione del backup per l'elemento in $PI \[ 0 \] e inserisce l'elemento in uno stato SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="342bb-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="342bb-113">Il quarto comando il nuovo elemento che si trova in uno stato SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="342bb-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="342bb-114">L'ultimo comando reidrata la VM SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="342bb-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="342bb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="342bb-115">PARAMETERS</span></span>

### <span data-ttu-id="342bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342bb-116">-DefaultProfile</span></span>
<span data-ttu-id="342bb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="342bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342bb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="342bb-118">-Force</span></span>
<span data-ttu-id="342bb-119">Force Disabilita la protezione del backup (impedisce la finestra di dialogo di conferma).</span><span class="sxs-lookup"><span data-stu-id="342bb-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="342bb-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="342bb-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="342bb-121">-Elemento</span><span class="sxs-lookup"><span data-stu-id="342bb-121">-Item</span></span>
<span data-ttu-id="342bb-122">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="342bb-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="342bb-123">Per ottenere un AzureRmRecoveryServicesBackupItem, usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="342bb-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="342bb-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="342bb-124">-VaultId</span></span>
<span data-ttu-id="342bb-125">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="342bb-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="342bb-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="342bb-126">-Confirm</span></span>
<span data-ttu-id="342bb-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="342bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="342bb-128">-WhatIf</span></span>
<span data-ttu-id="342bb-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="342bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="342bb-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="342bb-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342bb-131">CommonParameters</span></span>
<span data-ttu-id="342bb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342bb-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="342bb-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342bb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="342bb-134">INPUTS</span></span>

### <span data-ttu-id="342bb-135">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="342bb-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="342bb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="342bb-136">System.String</span></span>

## <span data-ttu-id="342bb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="342bb-137">OUTPUTS</span></span>

### <span data-ttu-id="342bb-138">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="342bb-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="342bb-139">Note</span><span class="sxs-lookup"><span data-stu-id="342bb-139">NOTES</span></span>

## <span data-ttu-id="342bb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="342bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="342bb-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="342bb-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="342bb-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="342bb-142">Get-AzRecoveryServicesBackupItem</span></span>]()

