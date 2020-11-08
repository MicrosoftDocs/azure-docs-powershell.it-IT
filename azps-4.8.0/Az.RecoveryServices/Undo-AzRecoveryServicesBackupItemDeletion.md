---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032821"
---
# <span data-ttu-id="95838-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="95838-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="95838-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95838-102">SYNOPSIS</span></span>
<span data-ttu-id="95838-103">Se un elemento di backup viene eliminato e presente in uno stato eliminato temporaneamente, questo comando riporta l'elemento in uno stato in cui i dati vengono conservati per sempre</span><span class="sxs-lookup"><span data-stu-id="95838-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="95838-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95838-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95838-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95838-105">DESCRIPTION</span></span>
<span data-ttu-id="95838-106">Il cmdlet Undo-AzRecoveryServicesBackupItemDeletion ripristina un elemento eliminato temporaneamente in uno stato in cui la protezione viene interrotta, ma i dati vengono mantenuti per sempre.</span><span class="sxs-lookup"><span data-stu-id="95838-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="95838-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95838-107">EXAMPLES</span></span>

### <span data-ttu-id="95838-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95838-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="95838-109">Il primo comando ottiene una matrice di contenitori di backup e lo archivia nella matrice $Cont.</span><span class="sxs-lookup"><span data-stu-id="95838-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="95838-110">Il secondo comando ottiene l'elemento di backup corrispondente al primo elemento contenitore e lo archivia nella variabile $PI.</span><span class="sxs-lookup"><span data-stu-id="95838-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="95838-111">Il terzo comando Disabilita la protezione del backup per l'elemento in $PI \[ 0 \] e inserisce l'elemento in uno stato SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="95838-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="95838-112">Il quarto comando ottiene l'elemento che si trova in uno stato SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="95838-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="95838-113">L'ultimo comando porta la VM SoftDeleted in uno stato in cui la protezione viene interrotta, ma i dati vengono mantenuti per sempre.</span><span class="sxs-lookup"><span data-stu-id="95838-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="95838-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="95838-114">Example 2</span></span>

<span data-ttu-id="95838-115">Reidrata un elemento eliminato temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="95838-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="95838-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="95838-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="95838-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95838-117">PARAMETERS</span></span>

### <span data-ttu-id="95838-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95838-118">-DefaultProfile</span></span>
<span data-ttu-id="95838-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95838-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95838-120">-Force</span><span class="sxs-lookup"><span data-stu-id="95838-120">-Force</span></span>
<span data-ttu-id="95838-121">Force Disabilita la protezione del backup (impedisce la finestra di dialogo di conferma).</span><span class="sxs-lookup"><span data-stu-id="95838-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="95838-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95838-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="95838-123">-Elemento</span><span class="sxs-lookup"><span data-stu-id="95838-123">-Item</span></span>
<span data-ttu-id="95838-124">Specifica l'elemento di backup per cui questo cmdlet ripristina l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="95838-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="95838-125">Per ottenere un AzureRmRecoveryServicesBackupItem, usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="95838-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="95838-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="95838-126">-VaultId</span></span>
<span data-ttu-id="95838-127">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="95838-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="95838-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95838-128">-Confirm</span></span>
<span data-ttu-id="95838-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95838-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95838-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95838-130">-WhatIf</span></span>
<span data-ttu-id="95838-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95838-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95838-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95838-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95838-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95838-133">CommonParameters</span></span>
<span data-ttu-id="95838-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95838-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95838-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95838-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95838-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95838-136">INPUTS</span></span>

### <span data-ttu-id="95838-137">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="95838-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="95838-138">System. String</span><span class="sxs-lookup"><span data-stu-id="95838-138">System.String</span></span>

## <span data-ttu-id="95838-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95838-139">OUTPUTS</span></span>

### <span data-ttu-id="95838-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="95838-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="95838-141">Note</span><span class="sxs-lookup"><span data-stu-id="95838-141">NOTES</span></span>

## <span data-ttu-id="95838-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95838-142">RELATED LINKS</span></span>

[<span data-ttu-id="95838-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="95838-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="95838-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="95838-144">Get-AzRecoveryServicesBackupItem</span></span>]()

