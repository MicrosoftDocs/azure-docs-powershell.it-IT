---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511316"
---
# <span data-ttu-id="34701-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="34701-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="34701-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34701-102">SYNOPSIS</span></span>
<span data-ttu-id="34701-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="34701-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34701-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34701-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34701-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34701-105">DESCRIPTION</span></span>
<span data-ttu-id="34701-106">Il cmdlet **Restore-AzureRmBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="34701-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="34701-107">Questo cmdlet avvia il ripristino dall'archivio di backup al proprio account.</span><span class="sxs-lookup"><span data-stu-id="34701-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="34701-108">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="34701-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="34701-109">Ripristina i dati del disco e le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="34701-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="34701-110">Al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="34701-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="34701-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34701-111">EXAMPLES</span></span>

### <span data-ttu-id="34701-112">Esempio 1: ripristinare una macchina virtuale in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="34701-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="34701-113">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="34701-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="34701-114">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="34701-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="34701-115">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="34701-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="34701-116">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="34701-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="34701-117">Il terzo comando ottiene l'elemento di backup nel contenitore in $Container usando il cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="34701-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="34701-118">Il comando Archivia l'oggetto nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="34701-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="34701-119">Il quarto comando ottiene il punto di ripristino per l'elemento in $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="34701-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="34701-120">Il comando Archivia l'oggetto nella variabile $RecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="34701-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="34701-121">Il comando finale ripristina il punto di recupero in $RecoveryPoint per l'account denominato DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="34701-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="34701-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34701-122">PARAMETERS</span></span>

### <span data-ttu-id="34701-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="34701-123">-RecoveryPoint</span></span>
<span data-ttu-id="34701-124">Specifica il punto di ripristino a cui ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34701-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="34701-125">Per ottenere un **AzureRmBackupRecoveryPoint** , usare il cmdlet Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="34701-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34701-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="34701-126">-StorageAccountName</span></span>
<span data-ttu-id="34701-127">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="34701-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="34701-128">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34701-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34701-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34701-129">-DefaultProfile</span></span>
<span data-ttu-id="34701-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34701-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34701-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34701-131">CommonParameters</span></span>
<span data-ttu-id="34701-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34701-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34701-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34701-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34701-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34701-134">INPUTS</span></span>

### <span data-ttu-id="34701-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="34701-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="34701-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34701-136">OUTPUTS</span></span>

### <span data-ttu-id="34701-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="34701-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="34701-138">Note</span><span class="sxs-lookup"><span data-stu-id="34701-138">NOTES</span></span>

## <span data-ttu-id="34701-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34701-139">RELATED LINKS</span></span>

[<span data-ttu-id="34701-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="34701-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="34701-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="34701-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="34701-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="34701-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


