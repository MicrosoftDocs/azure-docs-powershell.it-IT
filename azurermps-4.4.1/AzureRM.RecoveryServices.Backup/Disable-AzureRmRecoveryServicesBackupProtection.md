---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: a9caa2a40a6ae2ee6e29f6f24ff8266b73868fe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686802"
---
# <span data-ttu-id="64198-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="64198-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="64198-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64198-102">SYNOPSIS</span></span>
<span data-ttu-id="64198-103">Disabilita la protezione per un elemento protetto da backup.</span><span class="sxs-lookup"><span data-stu-id="64198-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64198-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64198-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64198-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64198-105">DESCRIPTION</span></span>
<span data-ttu-id="64198-106">Il cmdlet **Disable-AzureRmRecoveryServicesBackupProtection Disabilita** la protezione per un elemento protetto da backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="64198-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="64198-107">Questo cmdlet interrompe il backup pianificato regolare di un elemento.</span><span class="sxs-lookup"><span data-stu-id="64198-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="64198-108">Questo cmdlet può anche eliminare i punti di ripristino esistenti per l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="64198-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="64198-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="64198-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="64198-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64198-110">EXAMPLES</span></span>

### <span data-ttu-id="64198-111">Esempio 1: disabilitare la protezione del backup</span><span class="sxs-lookup"><span data-stu-id="64198-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="64198-112">Il primo comando ottiene una matrice di contenitori di backup e lo archivia nella matrice $Cont.</span><span class="sxs-lookup"><span data-stu-id="64198-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="64198-113">Il secondo comando ottiene l'elemento di backup corrispondente al primo elemento contenitore e lo archivia nella variabile $PI.</span><span class="sxs-lookup"><span data-stu-id="64198-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="64198-114">L'ultimo comando Disabilita la protezione del backup per l'elemento in $PI \[ 0 \] , ma mantiene i dati.</span><span class="sxs-lookup"><span data-stu-id="64198-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="64198-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64198-115">PARAMETERS</span></span>

### <span data-ttu-id="64198-116">-Force</span><span class="sxs-lookup"><span data-stu-id="64198-116">-Force</span></span>
<span data-ttu-id="64198-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64198-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64198-118">-Elemento</span><span class="sxs-lookup"><span data-stu-id="64198-118">-Item</span></span>
<span data-ttu-id="64198-119">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="64198-119">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="64198-120">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="64198-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="64198-121">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="64198-121">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="64198-122">Indica che questo cmdlet elimina i punti di ripristino esistenti.</span><span class="sxs-lookup"><span data-stu-id="64198-122">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="64198-123">Per eliminare i punti di ripristino archiviati in un secondo momento, eseguire di nuovo questo cmdlet e specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="64198-123">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="64198-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64198-124">-Confirm</span></span>
<span data-ttu-id="64198-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64198-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64198-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64198-126">-WhatIf</span></span>
<span data-ttu-id="64198-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64198-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64198-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64198-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64198-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64198-129">-DefaultProfile</span></span>
<span data-ttu-id="64198-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64198-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64198-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64198-131">CommonParameters</span></span>
<span data-ttu-id="64198-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64198-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64198-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64198-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64198-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64198-134">INPUTS</span></span>

### <span data-ttu-id="64198-135">ItemBase</span><span class="sxs-lookup"><span data-stu-id="64198-135">ItemBase</span></span>
<span data-ttu-id="64198-136">Il parametro ' Item ' accetta il valore di tipo ' ItemBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="64198-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="64198-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64198-137">OUTPUTS</span></span>

### <span data-ttu-id="64198-138">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="64198-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="64198-139">Note</span><span class="sxs-lookup"><span data-stu-id="64198-139">NOTES</span></span>

## <span data-ttu-id="64198-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64198-140">RELATED LINKS</span></span>

[<span data-ttu-id="64198-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="64198-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="64198-142">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64198-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="64198-143">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="64198-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


